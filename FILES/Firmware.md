here u can find the firmware (if u scroll down there is the code)

 <img width="1432" height="518" alt="image" src="https://github.com/user-attachments/assets/5d5ff368-102c-499e-aec9-87393b543fe3" />
import board
from kmk.modules.layers import Layers
from kmk.kmk_keyboard import KMKKeyboard
from kmk.keys import KC
from kmk.scanners import DiodeOrientation

keyboard = KMKKeyboard()

keyboard.col_pins = (board.GPI0,board.GPI01,board.GPI02,board.GPI03,board.GPI04,board.GPI05,board.GPI06,board.GPI07,board.GPI08,board.GPI09,board.GPI10,board.GPI11,board.GPI12,)
keyboard.row_pins = (board.GP16,board.GPI17,board.GPI18,board.GPI19,board.GPI20)
keyboard.diode_orientation = DiodeOrientation.COL2ROW
keyboard.modules.append(Layers())
keyboard.keymap = [
    [KC.SCLN, KC.N1,      KC.N2,  KC.GESC, KC.LGUI(KC.LSFT(KC.S)),KC.N5,   KC.N6,   KC.N7,   KC.N8,     KC.N9,     KC.N0,            KC.EQUAL,    KC.GRAVE,
     KC.TAB,  KC.Q,       KC.W,   KC.N3,   KC.E,                  KC.N4,   KC.R,    KC.T,    KC.Z,      KC.U,      KC.I,             KC.O,        KC.P,
     KC.CAPS, KC.A,       KC.S,   KC.D,    KC.F,                  KC.G,    KC.H,    KC.J,    KC.K,      KC.L,      KC.ů,             KC.KC.BSLASH,KC.QUOT
     KC.SHIFT,KC.LSHIFT,  KC.Y,   KC.X,    KC.C,                  KC.V,    KC.B,    KC.B,    KC.N,      KC.M,      KC.LSFT(KC.SLSH), KC.DOT,      KC.MINUS,
     KC.LCTL, KC.LGUI,    KC.LALT,KC.SPC,  KC.RALT,               KC.RGUI, KC.SLSH, KC.RCTL, KC.RSHIFT, KC.ENT,    KC.KC.SLASH,      KC.BSPC,     KC.MOMENTARY = KC.MO(1)],
    [KC.SCLN, KC.F1,      KC.F2,  KC.GESC, KC.LGUI(KC.LSFT(KC.S)),KC.F5,   KC.F6,   KC.F7,   KC.F8,     KC.F9,     KC.F10,           KC.EQUAL,    KC.GRAVE,
     KC.TAB,  KC.Q,       KC.W,   KC.F3,   KC.E,                  KC.F4,   KC.R,    KC.T,    KC.Z,      KC.U,      KC.I,             KC.O,        KC.P,
     KC.CAPS, KC.A,       KC.S,   KC.D,    KC.F,                  KC.G,    KC.H,    KC.J,    KC.K,      KC.L,      KC.ů,             KC.KC.BSLASH,KC.QUOT
     KC.SHIFT,KC.LSHIFT,  KC.Y,   KC.X,    KC.C,                  KC.V,    KC.B,    KC.B,    KC.N,      KC.M,      KC.LSFT(KC.SLSH), KC.DOT,      KC.MINUS,
     KC.LCTL, KC.LGUI,    KC.LALT,KC.SPC,  KC.RALT,               KC.RGUI, KC.SLSH, KC.RCTL, KC.RSHIFT, KC.ENT,    KC.SLASH,         KC.BSPC,     xxxxxxxx]
]

if __name__ == '__main__':
    keyboard.go()

