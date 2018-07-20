---
UID: NS:commctrl.tagTOOLINFOW
title: tagTOOLINFOW
author: windows-sdk-content
description: The TOOLINFO structure contains information about a tool in a tooltip control.
old-location: controls\TOOLINFO.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\tooltip\structures\toolinfo.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*LPTTTOOLINFOW, *PTOOLINFOW, LPTOOLINFO, LPTOOLINFO structure pointer [Windows Controls], PTOOLINFO, PTOOLINFO structure pointer [Windows Controls], TOOLINFO, TOOLINFO structure [Windows Controls], TOOLINFOA, TOOLINFOW, TTF_ABSOLUTE, TTF_CENTERTIP, TTF_IDISHWND, TTF_PARSELINKS, TTF_RTLREADING, TTF_SUBCLASS, TTF_TRACK, TTF_TRANSPARENT, TTTOOLINFO, TTTOOLINFOA, TTTOOLINFOW, _win32_TOOLINFO, _win32_TOOLINFO_cpp, commctrl/LPTOOLINFO, commctrl/PTOOLINFO, commctrl/TOOLINFO, commctrl/TOOLINFOA, commctrl/TOOLINFOW, controls.TOOLINFO, controls._win32_TOOLINFO, tagTOOLINFOW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TOOLINFOW (Unicode) and TOOLINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TTTOOLINFOW, *PTOOLINFOW, *LPTTTOOLINFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TOOLINFO
 - TOOLINFOA
 - TOOLINFOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagTOOLINFOW structure


## -description


The <b>TOOLINFO</b> structure contains information about a tool in a tooltip control.


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of this structure, in bytes. This member must be specified. 


### -field uFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flags that control the tooltip display. This member can be a combination of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TTF_ABSOLUTE"></a><a id="ttf_absolute"></a><dl>
<dt><b>TTF_ABSOLUTE</b></dt>
</dl>
</td>
<td width="60%">

                Positions the tooltip window at the same coordinates provided by <a href="https://msdn.microsoft.com/9eb7c86c-78e6-442a-ad77-5fb919cab591">TTM_TRACKPOSITION</a>. This flag must be used with the TTF_TRACK flag. 

</td>
</tr>
<tr>
<td width="40%"><a id="TTF_CENTERTIP"></a><a id="ttf_centertip"></a><dl>
<dt><b>TTF_CENTERTIP</b></dt>
</dl>
</td>
<td width="60%">
Centers the tooltip window below the tool specified by the <b>uId</b> member. 

</td>
</tr>
<tr>
<td width="40%"><a id="TTF_IDISHWND"></a><a id="ttf_idishwnd"></a><dl>
<dt><b>TTF_IDISHWND</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>uId</b> member is the window handle to the tool. If this flag is not set, <b>uId</b> is the tool's identifier. 

</td>
</tr>
<tr>
<td width="40%"><a id="TTF_PARSELINKS"></a><a id="ttf_parselinks"></a><dl>
<dt><b>TTF_PARSELINKS</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 6.0 and later</a>. Indicates that links in the tooltip text should be parsed.
                        
                        

Note that Comctl32.dll version 6 is not redistributable but it is included in Windows or later. To use Comctl32.dll version 6, specify it in a manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="TTF_RTLREADING"></a><a id="ttf_rtlreading"></a><dl>
<dt><b>TTF_RTLREADING</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the tooltip text will be displayed in the opposite direction to the text in the parent window. 

</td>
</tr>
<tr>
<td width="40%"><a id="TTF_SUBCLASS"></a><a id="ttf_subclass"></a><dl>
<dt><b>TTF_SUBCLASS</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the tooltip control should subclass the tool's window to intercept messages, such as <a href="https://msdn.microsoft.com/9b99387e-e176-4b20-a05a-bc75928a1367">WM_MOUSEMOVE</a>. If this flag is not set, you must use the <a href="https://msdn.microsoft.com/76d6d0ed-f357-479e-83d8-03d2e988cbd3">TTM_RELAYEVENT</a> message to forward messages to the tooltip control. For a list of messages that a tooltip control processes, see TTM_RELAYEVENT. 

</td>
</tr>
<tr>
<td width="40%"><a id="TTF_TRACK"></a><a id="ttf_track"></a><dl>
<dt><b>TTF_TRACK</b></dt>
</dl>
</td>
<td width="60%">

                Positions the tooltip window next to the tool to which it corresponds and moves the window according to coordinates supplied by the <a href="https://msdn.microsoft.com/9eb7c86c-78e6-442a-ad77-5fb919cab591">TTM_TRACKPOSITION</a> messages. You must activate this type of tool using the <a href="https://msdn.microsoft.com/6cf43377-a772-4749-81c4-a685998092e5">TTM_TRACKACTIVATE</a> message. 

</td>
</tr>
<tr>
<td width="40%"><a id="TTF_TRANSPARENT"></a><a id="ttf_transparent"></a><dl>
<dt><b>TTF_TRANSPARENT</b></dt>
</dl>
</td>
<td width="60%">

                Causes the tooltip control to forward mouse event messages to the parent window. This is limited to mouse events that occur within the bounds of the tooltip window. 

</td>
</tr>
</table>
 


### -field hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the window that contains the tool. If <b>lpszText</b> includes the LPSTR_TEXTCALLBACK value, this member identifies the window that receives the <a href="https://msdn.microsoft.com/af9ecc27-2004-4c45-9f1d-9ee0b2b50ff6">TTN_GETDISPINFO</a> notification codes.


### -field uId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT_PTR</a></b>

Application-defined identifier of the tool. If <b>uFlags</b> includes the TTF_IDISHWND flag, <b>uId</b> must specify the window handle to the tool. 


### -field rect

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

The bounding rectangle coordinates of the tool. The coordinates are relative to the upper-left corner of the client area of the window identified by <b>hwnd</b>. If <b>uFlags</b> includes the TTF_IDISHWND flag, this member is ignored. 


### -field hinst

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HINSTANCE</a></b>

Handle to the instance that contains the string resource for the tool. If <b>lpszText</b> specifies the identifier of a string resource, this member is used.


### -field lpszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

Pointer to the buffer that contains the text for the tool, or identifier of the string resource that contains the text. This member is sometimes used to return values. If you need to examine the returned value,  must point to a valid buffer of sufficient size. Otherwise, it can be set to <b>NULL</b>. If <b>lpszText</b> is set to LPSTR_TEXTCALLBACK, the control sends
the <a href="https://msdn.microsoft.com/af9ecc27-2004-4c45-9f1d-9ee0b2b50ff6">TTN_GETDISPINFO</a> notification code to the owner window to retrieve the text.


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

<b>Version 4.70 and later</b>. A 32-bit application-defined value that is associated with the tool. 


### -field lpReserved

Type: <b>void*</b>


            Reserved. Must be set to <b>NULL</b>.


## -remarks



Normal windows display text left-to-right (LTR). Windows can be <i>mirrored</i> to display languages such as Hebrew or Arabic that read right-to-left (RTL). Normally, tooltip text is displayed in the same direction as the text in its parent window. If TTF_RTLREADING is set, tooltip text will read in the opposite direction from the text in the parent window.



