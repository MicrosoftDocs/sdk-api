---
UID: NE:d2d1svg.D2D1_SVG_PATH_COMMAND
title: D2D1_SVG_PATH_COMMAND (d2d1svg.h)
description: Represents a path commmand. Each command may reference floats from the segment data. Commands ending in _ABSOLUTE interpret data as absolute coordinate. Commands ending in _RELATIVE interpret data as being relative to the previous point.
helpviewer_keywords: ["D2D1_SVG_PATH_COMMAND","D2D1_SVG_PATH_COMMAND enumeration [Direct2D]","D2D1_SVG_PATH_COMMAND_ARC_ABSOLUTE","D2D1_SVG_PATH_COMMAND_ARC_RELATIVE","D2D1_SVG_PATH_COMMAND_CLOSE_PATH","D2D1_SVG_PATH_COMMAND_CUBIC_ABSOLUTE","D2D1_SVG_PATH_COMMAND_CUBIC_RELATIVE","D2D1_SVG_PATH_COMMAND_CUBIC_SMOOTH_ABSOLUTE","D2D1_SVG_PATH_COMMAND_CUBIC_SMOOTH_RELATIVE","D2D1_SVG_PATH_COMMAND_FORCE_DWORD","D2D1_SVG_PATH_COMMAND_HORIZONTAL_ABSOLUTE","D2D1_SVG_PATH_COMMAND_HORIZONTAL_RELATIVE","D2D1_SVG_PATH_COMMAND_LINE_ABSOLUTE","D2D1_SVG_PATH_COMMAND_LINE_RELATIVE","D2D1_SVG_PATH_COMMAND_MOVE_ABSOLUTE","D2D1_SVG_PATH_COMMAND_MOVE_RELATIVE","D2D1_SVG_PATH_COMMAND_QUADRADIC_ABSOLUTE","D2D1_SVG_PATH_COMMAND_QUADRADIC_RELATIVE","D2D1_SVG_PATH_COMMAND_QUADRADIC_SMOOTH_ABSOLUTE","D2D1_SVG_PATH_COMMAND_QUADRADIC_SMOOTH_RELATIVE","D2D1_SVG_PATH_COMMAND_VERTICAL_ABSOLUTE","D2D1_SVG_PATH_COMMAND_VERTICAL_RELATIVE","d2d1svg/D2D1_SVG_PATH_COMMAND","d2d1svg/D2D1_SVG_PATH_COMMAND_ARC_ABSOLUTE","d2d1svg/D2D1_SVG_PATH_COMMAND_ARC_RELATIVE","d2d1svg/D2D1_SVG_PATH_COMMAND_CLOSE_PATH","d2d1svg/D2D1_SVG_PATH_COMMAND_CUBIC_ABSOLUTE","d2d1svg/D2D1_SVG_PATH_COMMAND_CUBIC_RELATIVE","d2d1svg/D2D1_SVG_PATH_COMMAND_CUBIC_SMOOTH_ABSOLUTE","d2d1svg/D2D1_SVG_PATH_COMMAND_CUBIC_SMOOTH_RELATIVE","d2d1svg/D2D1_SVG_PATH_COMMAND_FORCE_DWORD","d2d1svg/D2D1_SVG_PATH_COMMAND_HORIZONTAL_ABSOLUTE","d2d1svg/D2D1_SVG_PATH_COMMAND_HORIZONTAL_RELATIVE","d2d1svg/D2D1_SVG_PATH_COMMAND_LINE_ABSOLUTE","d2d1svg/D2D1_SVG_PATH_COMMAND_LINE_RELATIVE","d2d1svg/D2D1_SVG_PATH_COMMAND_MOVE_ABSOLUTE","d2d1svg/D2D1_SVG_PATH_COMMAND_MOVE_RELATIVE","d2d1svg/D2D1_SVG_PATH_COMMAND_QUADRADIC_ABSOLUTE","d2d1svg/D2D1_SVG_PATH_COMMAND_QUADRADIC_RELATIVE","d2d1svg/D2D1_SVG_PATH_COMMAND_QUADRADIC_SMOOTH_ABSOLUTE","d2d1svg/D2D1_SVG_PATH_COMMAND_QUADRADIC_SMOOTH_RELATIVE","d2d1svg/D2D1_SVG_PATH_COMMAND_VERTICAL_ABSOLUTE","d2d1svg/D2D1_SVG_PATH_COMMAND_VERTICAL_RELATIVE","direct2d.d2d1_svg_path_command"]
old-location: direct2d\d2d1_svg_path_command.htm
tech.root: Direct2D
ms.assetid: E0A5F435-F4FB-4CD3-84B3-962CB7B96446
ms.date: 12/05/2018
ms.keywords: D2D1_SVG_PATH_COMMAND, D2D1_SVG_PATH_COMMAND enumeration [Direct2D], D2D1_SVG_PATH_COMMAND_ARC_ABSOLUTE, D2D1_SVG_PATH_COMMAND_ARC_RELATIVE, D2D1_SVG_PATH_COMMAND_CLOSE_PATH, D2D1_SVG_PATH_COMMAND_CUBIC_ABSOLUTE, D2D1_SVG_PATH_COMMAND_CUBIC_RELATIVE, D2D1_SVG_PATH_COMMAND_CUBIC_SMOOTH_ABSOLUTE, D2D1_SVG_PATH_COMMAND_CUBIC_SMOOTH_RELATIVE, D2D1_SVG_PATH_COMMAND_FORCE_DWORD, D2D1_SVG_PATH_COMMAND_HORIZONTAL_ABSOLUTE, D2D1_SVG_PATH_COMMAND_HORIZONTAL_RELATIVE, D2D1_SVG_PATH_COMMAND_LINE_ABSOLUTE, D2D1_SVG_PATH_COMMAND_LINE_RELATIVE, D2D1_SVG_PATH_COMMAND_MOVE_ABSOLUTE, D2D1_SVG_PATH_COMMAND_MOVE_RELATIVE, D2D1_SVG_PATH_COMMAND_QUADRADIC_ABSOLUTE, D2D1_SVG_PATH_COMMAND_QUADRADIC_RELATIVE, D2D1_SVG_PATH_COMMAND_QUADRADIC_SMOOTH_ABSOLUTE, D2D1_SVG_PATH_COMMAND_QUADRADIC_SMOOTH_RELATIVE, D2D1_SVG_PATH_COMMAND_VERTICAL_ABSOLUTE, D2D1_SVG_PATH_COMMAND_VERTICAL_RELATIVE, d2d1svg/D2D1_SVG_PATH_COMMAND, d2d1svg/D2D1_SVG_PATH_COMMAND_ARC_ABSOLUTE, d2d1svg/D2D1_SVG_PATH_COMMAND_ARC_RELATIVE, d2d1svg/D2D1_SVG_PATH_COMMAND_CLOSE_PATH, d2d1svg/D2D1_SVG_PATH_COMMAND_CUBIC_ABSOLUTE, d2d1svg/D2D1_SVG_PATH_COMMAND_CUBIC_RELATIVE, d2d1svg/D2D1_SVG_PATH_COMMAND_CUBIC_SMOOTH_ABSOLUTE, d2d1svg/D2D1_SVG_PATH_COMMAND_CUBIC_SMOOTH_RELATIVE, d2d1svg/D2D1_SVG_PATH_COMMAND_FORCE_DWORD, d2d1svg/D2D1_SVG_PATH_COMMAND_HORIZONTAL_ABSOLUTE, d2d1svg/D2D1_SVG_PATH_COMMAND_HORIZONTAL_RELATIVE, d2d1svg/D2D1_SVG_PATH_COMMAND_LINE_ABSOLUTE, d2d1svg/D2D1_SVG_PATH_COMMAND_LINE_RELATIVE, d2d1svg/D2D1_SVG_PATH_COMMAND_MOVE_ABSOLUTE, d2d1svg/D2D1_SVG_PATH_COMMAND_MOVE_RELATIVE, d2d1svg/D2D1_SVG_PATH_COMMAND_QUADRADIC_ABSOLUTE, d2d1svg/D2D1_SVG_PATH_COMMAND_QUADRADIC_RELATIVE, d2d1svg/D2D1_SVG_PATH_COMMAND_QUADRADIC_SMOOTH_ABSOLUTE, d2d1svg/D2D1_SVG_PATH_COMMAND_QUADRADIC_SMOOTH_RELATIVE, d2d1svg/D2D1_SVG_PATH_COMMAND_VERTICAL_ABSOLUTE, d2d1svg/D2D1_SVG_PATH_COMMAND_VERTICAL_RELATIVE, direct2d.d2d1_svg_path_command
req.header: d2d1svg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_SVG_PATH_COMMAND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_SVG_PATH_COMMAND
 - d2d1svg/D2D1_SVG_PATH_COMMAND
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1svg.h
api_name:
 - D2D1_SVG_PATH_COMMAND
---

# D2D1_SVG_PATH_COMMAND enumeration


## -description

Represents a path commmand. Each command may reference floats from the segment data. Commands ending in _ABSOLUTE interpret data as absolute coordinate.
        Commands ending in _RELATIVE interpret data as being relative to the previous point.

## -enum-fields

### -field D2D1_SVG_PATH_COMMAND_CLOSE_PATH:0

Closes the current subpath. Uses no segment data.

### -field D2D1_SVG_PATH_COMMAND_MOVE_ABSOLUTE:1

Starts a new subpath at the coordinate (x y). Uses 2 floats of segment data.

### -field D2D1_SVG_PATH_COMMAND_MOVE_RELATIVE:2

Starts a new subpath at the coordinate (x y). Uses 2 floats of segment data.

### -field D2D1_SVG_PATH_COMMAND_LINE_ABSOLUTE:3

Draws a line to the coordinate (x y). Uses 2 floats of segment data.

### -field D2D1_SVG_PATH_COMMAND_LINE_RELATIVE:4

Draws a line to the coordinate (x y). Uses 2 floats of segment data.

### -field D2D1_SVG_PATH_COMMAND_CUBIC_ABSOLUTE:5

Draws a cubic Bezier curve (x1 y1 x2 y2 x y). The curve ends at (x, y) and is defined by the two control points (x1, y1) and (x2, y2). Uses 6 floats of segment data.

### -field D2D1_SVG_PATH_COMMAND_CUBIC_RELATIVE:6

Draws a cubic Bezier curve (x1 y1 x2 y2 x y). The curve ends at (x, y) and is defined by the two control points (x1, y1) and (x2, y2). Uses 6 floats of segment data.

### -field D2D1_SVG_PATH_COMMAND_QUADRADIC_ABSOLUTE:7

Draws a quadratic Bezier curve (x1 y1 x y). The curve ends at (x, y) and is defined by the control point (x1 y1). Uses 4 floats of segment data.

### -field D2D1_SVG_PATH_COMMAND_QUADRADIC_RELATIVE:8

Draws a quadratic Bezier curve (x1 y1 x y). The curve ends at (x, y) and is defined by the control point (x1 y1). Uses 4 floats of segment data.

### -field D2D1_SVG_PATH_COMMAND_ARC_ABSOLUTE:9

Draws an elliptical arc (rx ry x-axis-rotation large-arc-flag sweep-flag x y). The curve ends at (x, y) and is defined by the arc parameters. The two flags are
          considered set if their values are non-zero. Uses 7 floats of segment data.

### -field D2D1_SVG_PATH_COMMAND_ARC_RELATIVE:10

Draws an elliptical arc (rx ry x-axis-rotation large-arc-flag sweep-flag x y). The curve ends at (x, y) and is defined by the arc parameters. The two flags are
          considered set if their values are non-zero. Uses 7 floats of segment data.

### -field D2D1_SVG_PATH_COMMAND_HORIZONTAL_ABSOLUTE:11

Draws a horizontal line to the coordinate (x). Uses 1 float of segment data.

### -field D2D1_SVG_PATH_COMMAND_HORIZONTAL_RELATIVE:12

Draws a horizontal line to the coordinate (x). Uses 1 float of segment data.

### -field D2D1_SVG_PATH_COMMAND_VERTICAL_ABSOLUTE:13

Draws a vertical line to the coordinate (y). Uses 1 float of segment data.

### -field D2D1_SVG_PATH_COMMAND_VERTICAL_RELATIVE:14

Draws a vertical line to the coordinate (y). Uses 1 float of segment data.

### -field D2D1_SVG_PATH_COMMAND_CUBIC_SMOOTH_ABSOLUTE:15

Draws a smooth cubic Bezier curve (x2 y2 x y). The curve ends at (x, y) and is defined by the control point (x2, y2). Uses 4 floats of segment data.

### -field D2D1_SVG_PATH_COMMAND_CUBIC_SMOOTH_RELATIVE:16

Draws a smooth cubic Bezier curve (x2 y2 x y). The curve ends at (x, y) and is defined by the control point (x2, y2). Uses 4 floats of segment data.

### -field D2D1_SVG_PATH_COMMAND_QUADRADIC_SMOOTH_ABSOLUTE:17

Draws a smooth quadratic Bezier curve ending at (x, y). Uses 2 floats of segment data.

### -field D2D1_SVG_PATH_COMMAND_QUADRADIC_SMOOTH_RELATIVE:18

Draws a smooth quadratic Bezier curve ending at (x, y). Uses 2 floats of segment data.

### -field D2D1_SVG_PATH_COMMAND_FORCE_DWORD:0xffffffff

