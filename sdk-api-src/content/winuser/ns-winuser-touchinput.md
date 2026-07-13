---
UID: NS:winuser.tagTOUCHINPUT
title: TOUCHINPUT (winuser.h)
description: Encapsulates data for touch input.
old-location: wintouch\touchinput.htm
tech.root: wintouch
ms.assetid: fc382759-3a1e-401e-a6a7-1bf209a5434b
ms.date: 03/22/2022
ms.keywords: '*PTOUCHINPUT, PTOUCHINPUT, PTOUCHINPUT structure pointer [Windows Touch], TOUCHINPUT, TOUCHINPUT structure [Windows Touch], tagTOUCHINPUT, wintouch.touchinput, winuser/PTOUCHINPUT, winuser/TOUCHINPUT'
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
req.typenames: TOUCHINPUT, *PTOUCHINPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTOUCHINPUT
 - winuser/tagTOUCHINPUT
 - PTOUCHINPUT
 - winuser/PTOUCHINPUT
 - TOUCHINPUT
 - winuser/TOUCHINPUT
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
 - TOUCHINPUT
helpviewer_keywords: ["*PTOUCHINPUT","PTOUCHINPUT","PTOUCHINPUT structure pointer [Windows Touch]","TOUCHINPUT","TOUCHINPUT structure [Windows Touch]","tagTOUCHINPUT","wintouch.touchinput","winuser/PTOUCHINPUT","winuser/TOUCHINPUT"]
---

# TOUCHINPUT structure

## -description

Encapsulates data for touch input.

## -struct-fields

### -field x

The x-coordinate (horizontal point) of the touch input. This member is indicated in hundredths of a pixel of physical screen coordinates.

### -field y

The y-coordinate (vertical point) of the touch input. This member is indicated in hundredths of a pixel of physical screen coordinates.

### -field hSource

A device handle for the source input device.  Each device is given a unique provider at run time by the touch input provider. See **Examples** section below.

### -field dwID

A touch point identifier that distinguishes a particular touch input.  This value stays consistent in a touch contact sequence from the point a contact comes down until it comes back up. An ID may be reused later for subsequent contacts.

### -field dwFlags

A set of bit flags that specify various aspects of touch point press, release, and motion. The bits in this member can be any reasonable combination of the values in the Remarks section.

### -field dwMask

A set of bit flags that specify which of the optional fields in the structure contain valid values. The availability of valid information in the optional fields is device-specific. Applications should use an optional field value only when the corresponding bit is set in <i>dwMask</i>. This field may contain a combination of the <i>dwMask</i> flags mentioned in the Remarks section.

### -field dwTime

The time stamp for the event, in milliseconds.  The consuming application should note that the system performs no validation on this field; when the <b>TOUCHINPUTMASKF_TIMEFROMSYSTEM</b> flag is not set, the accuracy and sequencing of values in this field are completely dependent on the touch input provider.

### -field dwExtraInfo

An additional value associated with the touch event.

### -field cxContact

The width of the touch contact area in hundredths of a pixel in physical screen coordinates. This value is only valid if the <b>dwMask</b> member has the <b>TOUCHEVENTFMASK_CONTACTAREA</b> flag set.

### -field cyContact

The height of the touch contact area in hundredths of a pixel in physical screen coordinates. This value is only valid if the <b>dwMask</b> member has the <b>TOUCHEVENTFMASK_CONTACTAREA</b> flag set.

## -remarks

The following table lists the flags for the <b>dwFlags</b> member.
       <table>
<tr>
<th>Flag</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>TOUCHEVENTF_MOVE</b></td>
<td>0x0001</td>
<td>Movement has occurred. Cannot be combined with <b>TOUCHEVENTF_DOWN</b>.</td>
</tr>
<tr>
<td><b>TOUCHEVENTF_DOWN</b></td>
<td>0x0002</td>
<td>The corresponding touch point was established through a new contact. Cannot be combined with <b>TOUCHEVENTF_MOVE</b> or <b>TOUCHEVENTF_UP</b>.</td>
</tr>
<tr>
<td><b>TOUCHEVENTF_UP</b></td>
<td>0x0004</td>
<td>A touch point was removed.</td>
</tr>
<tr>
<td><b>TOUCHEVENTF_INRANGE</b></td>
<td>0x0008</td>
<td>A touch point is in range. This flag is used to enable touch hover support on compatible hardware. Applications that do not want support for hover can ignore this flag.</td>
</tr>
<tr>
<td><b>TOUCHEVENTF_PRIMARY</b></td>
<td>0x0010</td>
<td>Indicates that this <b>TOUCHINPUT</b> structure corresponds to a primary contact point. See the following text for more information on primary touch points.</td>
</tr>
<tr>
<td><b>TOUCHEVENTF_NOCOALESCE</b></td>
<td>0x0020</td>
<td>When received using <b>GetTouchInputInfo</b>, this input was not coalesced.</td>
</tr>
<tr>
<td><b>TOUCHEVENTF_PEN</b></td>
<td>0x0040</td>
<td>The touch event was triggered by a stylus device.</td>
</tr>
<tr>
<td><b>TOUCHEVENTF_PALM</b></td>
<td>0x0080</td>
<td>The touch event was triggered by the user's palm.</td>
</tr>
</table>
 



<div class="alert"><b>Note</b>     If the target hardware on a machine does not support hover, when the <b>TOUCHEVENTF_UP</b> flag is set, the <b>TOUCHEVENTF_INRANGE</b> flag is cleared.
   If the target hardware on a machine supports hover, the <b>TOUCHEVENTF_UP</b> and <b>TOUCHEVENTF_INRANGE</b> flags will be set independently.
   </div>
<div> </div>
The following table lists the flags for the <b>dwMask</b> member.
       <table>
<tr>
<th>Flag</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>TOUCHINPUTMASKF_CONTACTAREA</b></td>
<td>0x0004</td>
<td><b>cxContact</b> and <b>cyContact</b> are valid. See the following text for more information on primary touch points.</td>
</tr>
<tr>
<td><b>TOUCHINPUTMASKF_EXTRAINFO</b></td>
<td>0x0002</td>
<td><b>dwExtraInfo</b> is valid.</td>
</tr>
<tr>
<td><b>TOUCHINPUTMASKF_TIMEFROMSYSTEM</b></td>
<td>0x0001</td>
<td>The system time was set in the <b>TOUCHINPUT</b> structure.</td>
</tr>
</table>
 



A touch point is designated as primary when it is the first touch point to be established from a previous state of no touch points. 
   The <b>TOUCHEVENTF_PRIMARY</b> flag continues to be set for all subsequent events for the primary touch point until 
   the primary touch point is released. Note that a <b>TOUCHEVENTF_UP</b> event on the primary touch point does not 
   necessarily designate the end of a Windows Touch operation; the current Windows Touch operation proceeds from the establishment of the primary 
   touch point until the last touch point is released.
   

Note that a solitary touch point or, in a set of simultaneous touch points, the first to be detected, is designated the primary. The system mouse position follows the primary touch point and, in addition to touch messages, also generates <b>WM_LBUTTONDOWN</b>, <b>WM_MOUSEMOVE</b>, and <b>WM_LBUTTONUP</b> messages in response to actions on a primary touch point. The primary touch point can also generate <b>WM_RBUTTONDOWN</b> and <b>WM_RBUTTONUP</b> messages using the press and hold gesture.

Note that the touch point identifier may be dynamic and is associated with a given touch point only as long as the touch point persists. If contact is broken and then resumed (for example, if a finger is removed from the surface and then pressed down again), the same touch point (the same finger, pen, or other such device) may receive a different touch point identifier.

The following type is defined to represent a constant pointer to a <b>TOUCHINPUT</b> structure.
    


``` syntax

   typedef TOUCHINPUT const * PCTOUCHINPUT;
    
```


#### Examples

<div class="alert"><b>Note</b>  In the following example, the <i>pInputs</i> array is not sorted. Use the <b>dwID</b> value to track specific touch points.</div>
<div> </div>

```cpp
UINT cInputs = LOWORD(wParam);
PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
if (NULL != pInputs)
{
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
                          cInputs,
                          pInputs,
                          sizeof(TOUCHINPUT)))
    {
        // process pInputs
        if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
        {
            // error handling
        }
    }
    else
    {
        // GetLastError() and error handling
    }
    delete [] pInputs;
}
else
{
    // error handling, presumably out of memory
}
return DefWindowProc(hWnd, message, wParam, lParam);

```


The following example shows how to get the device information from the <b>hSource</b> member.  This example uses <a href="/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa">GetRawInputDevice</a> to retrieve information about the device.


```cpp
for (UINT i = 0; i < cInputs; i++){
  TOUCHINPUT ti = pInputs[i];      
  RID_DEVICE_INFO info;
  ZeroMemory(&info, sizeof(RID_DEVICE_INFO));
  info.cbSize = sizeof(RID_DEVICE_INFO);
  UINT size = 0;
  if (GetRawInputDeviceInfo(ti.hSource, RIDI_DEVICEINFO, &info, &size)){
  }else{
    DWORD err = GetLastError();
  }
}

```

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo">GetTouchInputInfo</a>



<a href="/windows/desktop/wintouch/structures">Structures</a>
