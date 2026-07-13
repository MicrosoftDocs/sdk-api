---
UID: NS:rectypes.tagRECO_GUIDE
title: RECO_GUIDE (rectypes.h)
description: Defines the boundaries of the ink to the recognizer.
helpviewer_keywords: ["RECO_GUIDE","RECO_GUIDE structure [Tablet PC]","e28347aa-08ed-4f40-b9c3-4d3b5dacbeb7","rectypes/RECO_GUIDE","tablet.reco_guide"]
old-location: tablet\reco_guide.htm
tech.root: tablet
ms.assetid: e28347aa-08ed-4f40-b9c3-4d3b5dacbeb7
ms.date: 12/05/2018
ms.keywords: RECO_GUIDE, RECO_GUIDE structure [Tablet PC], e28347aa-08ed-4f40-b9c3-4d3b5dacbeb7, rectypes/RECO_GUIDE, tablet.reco_guide
req.header: rectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: RECO_GUIDE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRECO_GUIDE
 - rectypes/tagRECO_GUIDE
 - RECO_GUIDE
 - rectypes/RECO_GUIDE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rectypes.h
api_name:
 - RECO_GUIDE
---

# RECO_GUIDE structure


## -description

Defines the boundaries of the ink to the recognizer.

## -struct-fields

### -field xOrigin

Left edge of the first box in ink space coordinates.

### -field yOrigin

Top edge of first box in ink-space coordinates.

### -field cxBox

Width of each box in ink space units.

### -field cyBox

Height of each box in ink-space units.

### -field cxBase

Margin to the guideline. This is one-half the distance in ink-space units between adjacent boxes.

### -field cyBase

Vertical distance in ink-space units from the baseline to the top of the box.

### -field cHorzBox

Count of columns of boxes.

### -field cVertBox

Count of rows of boxes.

### -field cyMid

Distance in ink-space units from the baseline to the midline, or 0 if the midline is not present.

## -remarks

If the application has drawn guidelines on the screen on which the user is expected to write, the application should set the values in the <b>RECO_GUIDE</b> structure to inform the recognizer. The <b>RECO_GUIDE</b> structure is for the recognizer's use only. Setting the <b>RECO_GUIDE</b> structure does not, by itself, draw visual clues on the display. The application or the control draws the visual clues.

The xOrigin and yOrigin members are ink-space coordinates of the upper-left corner of the area to write in. The cyBox and cxBox members are the height and width of the individual boxes to write in. If the guide is lined, they cyBox and cxBox width/height of every line. The cHorzBox and cVertBox members specify the number of columns and rows. The cyBase member specifies a baseline within the box. Setting the cyBase member to 0 indicates that there is no baseline. The cxBase member gives a horizontal displacement of the edge of the guideline from the edge of the box where writing is expected to start.

Use the values of cHorzBox and cVertBox to control the kind of recognition input that you use. When cHorzBox and cVertBox are both greater than zero, boxed input is used. The following table lists potential input modes and which values to set cHorzBox and cVertBox for each mode.

<table>
<tr>
<th>For this type of input</th>
<th>Set cHorzBox equal to</th>
<th>And set cVertBox equal to</th>
</tr>
<tr>
<td>
Free input

</td>
<td>
0

</td>
<td>
0

</td>
</tr>
<tr>
<td>
Lined input with 1 horizontal line

</td>
<td>
0

</td>
<td>
1

</td>
</tr>
<tr>
<td>
Lined input with 1 vertical line

</td>
<td>
1

</td>
<td>
0

</td>
</tr>
<tr>
<td>
Lined input with n horizontal lines

</td>
<td>
0

</td>
<td>
n

</td>
</tr>
<tr>
<td>
Lined input with n vertical lines

</td>
<td>
n

</td>
<td>
0

</td>
</tr>
<tr>
<td>
Boxed input with 1 box

</td>
<td>
1

</td>
<td>
1

</td>
</tr>
<tr>
<td>
Boxed input in a horizontal line with n boxes

</td>
<td>
n

</td>
<td>
1

</td>
</tr>
<tr>
<td>
Boxed input in a grid of boxes x rows by z columns

</td>
<td>
z

</td>
<td>
x

</td>
</tr>
</table>
 

The following illustration represents the recognition guide structure for five columns and three rows of boxes.

<img alt="Illustration of recognition guide structure" border="" src="images/3551c7eb-7398-4724-9de7-191818f35443.gif"/>
The following illustration represents a single box from the previous illustration.

<img alt="Illustration of single recognition guide box" border="" src="images/a7106d81-4314-44ec-905d-1bb3ba7711b7.gif"/>

## -see-also

<a href="/windows/desktop/api/recapis/nf-recapis-getguide">GetGuide Function</a>



<a href="/windows/desktop/api/recapis/nf-recapis-setguide">SetGuide Function</a>