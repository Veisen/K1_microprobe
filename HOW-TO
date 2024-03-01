add to printer.cfg

[gcode_macro SAFE_MOVE_Z]
gcode:
    G90
    {% if printer.toolhead.homed_axes != "x" %} # If X-Axis not homed.
		M117 Homing X-Axis...
		G28 X0
        {% if printer.toolhead.homed_axes != "y" %} # If Y-Axis not homed.
        M117 Homing Y-Axis...
		G28 Y0
        {% endif %}
	{% endif %}
    SAVE_GCODE_STATE NAME=previous_homing_positions
    G0 X280 Y30 F4500.0 # Move to Z-Offsets.
    G28 Z0 # Home Z-Axis.
    G0 Z5.0 F600.0 # Raise Z-Axis 5.0mm.
    RESTORE_GCODE_STATE NAME=previous_homing_positions MOVE=1 MOVE_SPEED=75.0

[gcode_macro SET_Z_OFFSET]
gcode:
  SET_GCODE_OFFSET Z=0

add to gcode_macro.cfg

[gcode_macro SAFE_MOVE_Z]
gcode:
    G90
    {% if printer.toolhead.homed_axes != "x" %} # If X-Axis not homed.
		M117 Homing X-Axis...
		G28 X0
        {% if printer.toolhead.homed_axes != "y" %} # If Y-Axis not homed.
        M117 Homing Y-Axis...
		G28 Y0
        {% endif %}
	{% endif %}
    SAVE_GCODE_STATE NAME=previous_homing_positions
    G0 X280 Y30 F4500.0 # Move to Z-Offsets.
    G28 Z0 # Home Z-Axis.
    G0 Z5.0 F600.0 # Raise Z-Axis 5.0mm.
    RESTORE_GCODE_STATE NAME=previous_homing_positions MOVE=1 MOVE_SPEED=75.0

[gcode_macro SET_Z_OFFSET]
gcode:
  SET_GCODE_OFFSET Z=0


replace file custom_macro.py in /usr/share/klipper/klippy/extras

replace file mcu.py in /usr/share/klipper/klippy
