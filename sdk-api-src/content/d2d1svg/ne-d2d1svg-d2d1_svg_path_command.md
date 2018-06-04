---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D2D1_SVG_PATH_COMMAND enumeration


## -description


Represents a path commmand. Each command may reference floats from the segment data. Commands ending in _ABSOLUTE interpret data as absolute coordinate.
        Commands ending in _RELATIVE interpret data as being relative to the previous point.


## -enum-fields




### -field D2D1_SVG_PATH_COMMAND_CLOSE_PATH

Closes the current subpath. Uses no segment data.


### -field D2D1_SVG_PATH_COMMAND_MOVE_ABSOLUTE

Starts a new subpath at the coordinate (x y). Uses 2 floats of segment data.


### -field D2D1_SVG_PATH_COMMAND_MOVE_RELATIVE

Starts a new subpath at the coordinate (x y). Uses 2 floats of segment data.


### -field D2D1_SVG_PATH_COMMAND_LINE_ABSOLUTE

Draws a line to the coordinate (x y). Uses 2 floats of segment data.


### -field D2D1_SVG_PATH_COMMAND_LINE_RELATIVE

Draws a line to the coordinate (x y). Uses 2 floats of segment data.


### -field D2D1_SVG_PATH_COMMAND_CUBIC_ABSOLUTE

Draws a cubic Bezier curve (x1 y1 x2 y2 x y). The curve ends at (x, y) and is defined by the two control points (x1, y1) and (x2, y2). Uses 6 floats of segment data.


### -field D2D1_SVG_PATH_COMMAND_CUBIC_RELATIVE

Draws a cubic Bezier curve (x1 y1 x2 y2 x y). The curve ends at (x, y) and is defined by the two control points (x1, y1) and (x2, y2). Uses 6 floats of segment data.


### -field D2D1_SVG_PATH_COMMAND_QUADRADIC_ABSOLUTE

Draws a quadratic Bezier curve (x1 y1 x y). The curve ends at (x, y) and is defined by the control point (x1 y1). Uses 4 floats of segment data.


### -field D2D1_SVG_PATH_COMMAND_QUADRADIC_RELATIVE

Draws a quadratic Bezier curve (x1 y1 x y). The curve ends at (x, y) and is defined by the control point (x1 y1). Uses 4 floats of segment data.


### -field D2D1_SVG_PATH_COMMAND_ARC_ABSOLUTE

Draws an elliptical arc (rx ry x-axis-rotation large-arc-flag sweep-flag x y). The curve ends at (x, y) and is defined by the arc parameters. The two flags are
          considered set if their values are non-zero. Uses 7 floats of segment data.


### -field D2D1_SVG_PATH_COMMAND_ARC_RELATIVE

Draws an elliptical arc (rx ry x-axis-rotation large-arc-flag sweep-flag x y). The curve ends at (x, y) and is defined by the arc parameters. The two flags are
          considered set if their values are non-zero. Uses 7 floats of segment data.


### -field D2D1_SVG_PATH_COMMAND_HORIZONTAL_ABSOLUTE

Draws a horizontal line to the coordinate (x). Uses 1 float of segment data.


### -field D2D1_SVG_PATH_COMMAND_HORIZONTAL_RELATIVE

Draws a horizontal line to the coordinate (x). Uses 1 float of segment data.


### -field D2D1_SVG_PATH_COMMAND_VERTICAL_ABSOLUTE

Draws a vertical line to the coordinate (y). Uses 1 float of segment data.


### -field D2D1_SVG_PATH_COMMAND_VERTICAL_RELATIVE

Draws a vertical line to the coordinate (y). Uses 1 float of segment data.


### -field D2D1_SVG_PATH_COMMAND_CUBIC_SMOOTH_ABSOLUTE

Draws a smooth cubic Bezier curve (x2 y2 x y). The curve ends at (x, y) and is defined by the control point (x2, y2). Uses 4 floats of segment data.


### -field D2D1_SVG_PATH_COMMAND_CUBIC_SMOOTH_RELATIVE

Draws a smooth cubic Bezier curve (x2 y2 x y). The curve ends at (x, y) and is defined by the control point (x2, y2). Uses 4 floats of segment data.


### -field D2D1_SVG_PATH_COMMAND_QUADRADIC_SMOOTH_ABSOLUTE

Draws a smooth quadratic Bezier curve ending at (x, y). Uses 2 floats of segment data.


### -field D2D1_SVG_PATH_COMMAND_QUADRADIC_SMOOTH_RELATIVE

Draws a smooth quadratic Bezier curve ending at (x, y). Uses 2 floats of segment data.


### -field D2D1_SVG_PATH_COMMAND_FORCE_DWORD

