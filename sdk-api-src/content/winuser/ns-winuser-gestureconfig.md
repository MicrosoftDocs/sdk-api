---
UID: NS:winuser.tagGESTURECONFIG
title: GESTURECONFIG (winuser.h)
description: Gets and sets the configuration for enabling gesture messages and the type of this configuration.
helpviewer_keywords: ["*PGESTURECONFIG","GESTURECONFIG","GESTURECONFIG structure [Windows Touch]","PGESTURECONFIG","PGESTURECONFIG structure pointer [Windows Touch]","tagGESTURECONFIG","wintouch.gestureconfig","winuser/GESTURECONFIG","winuser/PGESTURECONFIG"]
old-location: wintouch\gestureconfig.htm
tech.root: wintouch
ms.assetid: 4ec5050e-7fef-4f52-89af-5237e8cdbdb8
ms.date: 12/05/2018
ms.keywords: '*PGESTURECONFIG, GESTURECONFIG, GESTURECONFIG structure [Windows Touch], PGESTURECONFIG, PGESTURECONFIG structure pointer [Windows Touch], tagGESTURECONFIG, wintouch.gestureconfig, winuser/GESTURECONFIG, winuser/PGESTURECONFIG'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: GESTURECONFIG, *PGESTURECONFIG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagGESTURECONFIG
 - winuser/tagGESTURECONFIG
 - PGESTURECONFIG
 - winuser/PGESTURECONFIG
 - GESTURECONFIG
 - winuser/GESTURECONFIG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winuser.h
api_name:
 - GESTURECONFIG
---

# GESTURECONFIG structure


## -description

Gets and sets the configuration for 
  enabling gesture messages and the type of this configuration.

## -struct-fields

### -field dwID

The identifier for the type of configuration that will have messages enabled or disabled. For more information, see Remarks.

### -field dwWant

The messages to enable.

### -field dwBlock

The messages to disable.

## -remarks

It is impossible to disable two-finger panning and keep single finger panning.
      You must set the want bits for GC_PAN before you can set them for GC_PAN_WITH_SINGLE_FINGER_HORIZONTALLY 
		or GC_PAN_WITH_SINGLE_FINGER_VERTICALLY.
		

An inertia vector is included in the GID_PAN message with the GF_END flag if inertia was disabled by a call to 
		<a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig">SetGestureConfig</a>.
		

When you pass this structure, the <i>dwID</i> member contains information 
  for a set of gestures. This determines what the other flags will mean.
  If you set flags for pan messages, they will be different from those
  flags that are set for rotation messages.
  

The following table indicates the various identifiers for gestures that are
  supported by the <i>dwID</i> member of the <b>GESTURECONFIG</b> structure.  Note that setting
  <i>dwID</i> to 0 indicates that global gesture configuration flags are set.
  

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>GID_ZOOM</td>
<td>3</td>
<td>Indicates configuration settings for the zoom gesture.</td>
</tr>
<tr>
<td>GID_PAN</td>
<td>4</td>
<td>Indicates the pan gesture.</td>
</tr>
<tr>
<td>GID_ROTATE</td>
<td>5</td>
<td>Indicates the rotation gesture.</td>
</tr>
<tr>
<td>GID_TWOFINGERTAP</td>
<td>6</td>
<td>Indicates the two-finger tap gesture.</td>
</tr>
<tr>
<td>GID_PRESSANDTAP</td>
<td>7</td>
<td>Indicates the press and tap gesture.</td>
</tr>
</table>
 

The following flags are used when <i>dwID</i> is set to 0.

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>GC_ALLGESTURES</td>
<td>0x00000001</td>
<td>Indicates all of the gestures.</td>
</tr>
</table>
 

The following flags are used when <i>dwID</i> is set to GID_ZOOM.

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>GC_ZOOM</td>
<td>0x00000001</td>
<td>Indicates the zoom gesture.</td>
</tr>
</table>
 

The following flags are used when <i>dwID</i> is set to GID_PAN.

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>GC_PAN</td>
<td>0x00000001</td>
<td>Indicates all pan gestures.</td>
</tr>
<tr>
<td>GC_PAN_WITH_SINGLE_FINGER_VERTICALLY</td>
<td>0x00000002</td>
<td>Indicates vertical pans with one finger.</td>
</tr>
<tr>
<td>GC_PAN_WITH_SINGLE_FINGER_HORIZONTALLY</td>
<td>0x00000004</td>
<td>Indicates horizontal pans with one finger.</td>
</tr>
<tr>
<td>GC_PAN_WITH_GUTTER</td>
<td>0x00000008</td>
<td>Limits perpendicular movement to primary direction until a threshold is reached to break out of the gutter.</td>
</tr>
<tr>
<td>GC_PAN_WITH_INERTIA</td>
<td>0x00000010</td>
<td>Indicates panning with inertia to smoothly slow when pan gestures stop.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Setting the <b>GID_PAN</b> flags in <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig">SetGestureConfig</a> will affect the default gesture handler for panning.
    You should not have both <b>dwWant</b> and <b>dwBlock</b> set for the same flags; this will result in unexpected behavior.  
    See  <a href="/windows/desktop/wintouch/guide-multi-touch-gestures">Windows Touch Gestures</a> for more information on panning 
    and legacy panning support; see <b>SetGestureConfig</b> for examples  of enabling and blocking gestures.</div>
<div> </div>
The following flags are used when <i>dwID</i> is set to GID_ROTATE.

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>GC_ROTATE</td>
<td>0x00000001</td>
<td>Indicates the rotation gesture.</td>
</tr>
</table>
 

The following flags are used when <i>dwID</i> is set to GID_TWOFINGERTAP.

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>GC_TWOFINGERTAP</td>
<td>0x00000001</td>
<td>Indicates the two-finger tap gesture.</td>
</tr>
</table>
 

The following flags are used when <i>dwID</i> is set to GID_PRESSANDTAP.

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>GC_PRESSANDTAP</td>
<td>0x00000001</td>
<td>Indicates the press and tap gesture.</td>
</tr>
</table>
 


#### Examples


```cpp
    GESTURECONFIG gc[3];    
    UINT uiGcs = 3;

    ZeroMemory(&gc, sizeof(gc));
    gc[0].dwID  = GID_ZOOM;
    gc[1].dwID  = GID_ROTATE;
    gc[2].dwID  = GID_PAN;
    BOOL bResult = GetGestureConfig(hWnd, 0, 0, &uiGcs, gc, sizeof(GESTURECONFIG));        
    if (!bResult){                
        DWORD err = GetLastError();                                       
    }    

```

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getgestureconfig">GetGestureConfig</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig">SetGestureConfig</a>



<a href="/windows/desktop/wintouch/mtstructures">Structures</a>