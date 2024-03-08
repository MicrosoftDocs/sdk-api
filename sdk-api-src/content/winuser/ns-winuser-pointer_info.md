---
UID: NS:winuser.tagPOINTER_INFO
title: POINTER_INFO (winuser.h)
description: Contains basic pointer information common to all pointer types. Applications can retrieve this information using the GetPointerInfo, GetPointerFrameInfo, GetPointerInfoHistory and GetPointerFrameInfoHistory functions.
helpviewer_keywords: ["POINTER_INFO","POINTER_INFO structure [Input Messages and Notifications]","_POINTER_INFO","inputmsg.pointer_info_struct","winuser/POINTER_INFO"]
old-location: inputmsg\pointer_info_struct.htm
tech.root: InputMsg
ms.assetid: fee176ba-ad07-4145-0b4d-1b8c335fd102
ms.date: 12/05/2018
ms.keywords: POINTER_INFO, POINTER_INFO structure [Input Messages and Notifications], _POINTER_INFO, inputmsg.pointer_info_struct, winuser/POINTER_INFO
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: POINTER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPOINTER_INFO
 - winuser/tagPOINTER_INFO
 - POINTER_INFO
 - winuser/POINTER_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - POINTER_INFO
---

# POINTER_INFO structure


## -description

Contains basic pointer information common to all pointer types. Applications can retrieve this information using the <a href="/windows/desktop/api/winuser/nf-winuser-getpointerinfo">GetPointerInfo</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getpointerframeinfo">GetPointerFrameInfo</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getpointerinfohistory">GetPointerInfoHistory</a> and <a href="/windows/desktop/api/winuser/nf-winuser-getpointerframeinfohistory">GetPointerFrameInfoHistory</a> functions.

## -struct-fields

### -field pointerType

Type: <b><a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">POINTER_INPUT_TYPE</a></b>

A value from the <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">POINTER_INPUT_TYPE</a> enumeration that specifies the pointer type.

### -field pointerId

Type: <b>UINT32</b>

An identifier that uniquely identifies a pointer during its lifetime. A pointer comes into existence when it is first detected and ends its existence when it goes out of detection range. Note that if a physical entity (finger or pen) goes out of detection range and then returns to be detected again, it is treated as a new pointer and may be assigned a new pointer identifier.

### -field frameId

Type: <b>UINT32</b>

An identifier common to multiple pointers for which the source device reported an update in a single input frame. For example, a parallel-mode multi-touch digitizer may report the positions of multiple touch contacts in a single update to the system.

Note that frame identifier is assigned as input is reported to the system for all pointers across all devices. Therefore, this field may not contain strictly sequential values in a single series of messages that a window receives. However, this field will contain the same numerical value for all input updates that were reported in the same input frame by a single device.

### -field pointerFlags

Type: <b><a href="/windows/win32/inputmsg/pointer-flags-contants">POINTER_FLAGS</a></b>

May be any reasonable combination of flags from the <a href="/windows/win32/inputmsg/pointer-flags-contants">Pointer Flags</a> constants.

### -field sourceDevice

Type: <b>HANDLE</b>

Handle to the source device that can be used in calls to the raw input device API and the digitizer device API.

### -field hwndTarget

Type: <b>HWND</b>

Window to which this message was targeted. If the pointer is captured, either implicitly by virtue of having made contact over this window or explicitly using the pointer capture API, this is the capture window. If the pointer is uncaptured, this is the window over which the pointer was when this message was generated.

### -field ptPixelLocation

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The predicted screen coordinates of the pointer, in pixels. 

The predicted value is based on the pointer position reported by the digitizer and the motion of the pointer. This correction can compensate for visual lag due to inherent delays in sensing and processing the pointer location on the digitizer. This is applicable to  pointers of type <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_TOUCH</a>. For other pointer types, the predicted value will be the same as the non-predicted value (see <b>ptPixelLocationRaw</b>).

### -field ptHimetricLocation

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The predicted screen coordinates of the pointer, in HIMETRIC units. 

The predicted value is based on the pointer position reported by the digitizer and the motion of the pointer. This correction can compensate for visual lag due to inherent delays in sensing and processing the pointer location on the digitizer. This is applicable to  pointers of type <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_TOUCH</a>. For other pointer types, the predicted value will be the same as the non-predicted value (see <b>ptHimetricLocationRaw</b>).

### -field ptPixelLocationRaw

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The screen coordinates of the pointer, in pixels. For adjusted screen coordinates, see <b>ptPixelLocation</b>.

### -field ptHimetricLocationRaw

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The screen coordinates of the pointer, in HIMETRIC units. For adjusted screen coordinates, see <b>ptHimetricLocation</b>.

### -field dwTime

Type: <b>DWORD</b>

0 or the time stamp of the message, based on the system tick count when the message was received. 

The application can specify the input time stamp in either <b>dwTime</b> or <b>PerformanceCount</b>. The value cannot be more recent than the current tick count or <b>QueryPerformanceCount (QPC)</b> value of the injection thread. Once a frame is injected with a time stamp, all subsequent frames must include a timestamp until all contacts in the frame go to an <a href="/windows/desktop/api/winuser/ne-winuser-pointer_button_change_type">UP</a> state. The custom timestamp value must also be provided for the first element in the contacts array. The time stamp values after the first element are ignored. The custom timestamp value must increment in every injection frame.



When <b>PerformanceCount</b> is specified, the time stamp will be converted to the current time in .1 millisecond resolution upon actual injection. If a custom <b>PerformanceCount</b> resulted in the same .1 millisecond window from the previous injection, <b>ERROR_NOT_READY</b> is returned and injection will not occur. While injection will not be invalidated immediately by the error, the next successful injection must have a <b>PerformanceCount</b> value that is at least 0.1 millisecond from the previously successful injection. This is also true if <b>dwTime</b> is used.

If both <b>dwTime</b> and <b>PerformanceCount</b> are specified in <a href="/windows/desktop/api/winuser/nf-winuser-injecttouchinput">InjectTouchInput</a>, ERROR_INVALID_PARAMETER is returned. 


<a href="/windows/desktop/api/winuser/nf-winuser-injecttouchinput">InjectTouchInput</a> cannot switch between <b>dwTime</b> and <b>PerformanceCount</b> once injection has started.



If neither <b>dwTime</b> and <b>PerformanceCount</b> are specified, <a href="/windows/desktop/api/winuser/nf-winuser-injecttouchinput">InjectTouchInput</a> allocates the timestamp based on the timing of the call. If <b>InjectTouchInput</b> calls are  repeatedly less than 0.1 millisecond apart, ERROR_NOT_READY might be returned. The error will not invalidate the input immediately, but the injection application needs to retry the same frame again for injection to succeed.

### -field historyCount

Type: <b>UINT32</b>

Count of inputs that were coalesced into this message. This count matches the total count of entries that can be returned by a call to <a href="/windows/desktop/api/winuser/nf-winuser-getpointerinfohistory">GetPointerInfoHistory</a>. If no coalescing occurred, this count is 1 for the single input represented by the message.

### -field InputData

### -field dwKeyStates

Type: <b>DWORD</b>

 Indicates which keyboard modifier keys were pressed at the time the input was generated. May be zero, or a combination of the following values from [Modifier Key State](/windows/win32/inputmsg/modifier-key-states-constants).


POINTER_MOD_SHIFT – A SHIFT key was pressed.


POINTER_MOD_CTRL – A CTRL key was pressed.

Use <a href="/windows/desktop/api/winuser/nf-winuser-getkeystate">GetKeyState</a>.

### -field PerformanceCount

Type: <b>UINT64</b>

The value of the high-resolution performance counter when the pointer message was received (high-precision, 64 bit alternative to <b>dwTime</b>). The value can be calibrated when the touch digitizer hardware supports the scan timestamp information in its input report.

### -field ButtonChangeType

Type: <b>POINTER_BUTTON_CHANGE_TYPE</b>

A value from the <a href="/windows/desktop/api/winuser/ne-winuser-pointer_button_change_type">POINTER_BUTTON_CHANGE_TYPE</a> enumeration that specifies the change in button state between this input and the previous input.

### -field inputData

Type: <b>INT32</b>

 A value whose meaning depends on the nature of input.


When flags indicate <b>POINTER_FLAG_WHEEL</b>, this value indicates the distance the wheel is rotated, expressed in multiples or factors of WHEEL_DELTA. A positive value indicates that the wheel was rotated forward and a negative value indicates that the wheel was rotated backward.


When flags indicate <b>POINTER_FLAG_HWHEEL,</b> this value indicates the distance the wheel is rotated, expressed in multiples or factors of WHEEL_DELTA. A positive value indicates that the wheel was rotated to the right and a negative value indicates that the wheel was rotated to the left.

## -see-also


<a href="/windows/win32/inputmsg/structures">Structures</a>
