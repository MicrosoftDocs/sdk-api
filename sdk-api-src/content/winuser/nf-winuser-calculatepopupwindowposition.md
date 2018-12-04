---
UID: NF:winuser.CalculatePopupWindowPosition
title: CalculatePopupWindowPosition function
author: windows-sdk-content
description: Calculates an appropriate pop-up window position using the specified anchor point, pop-up window size, flags, and the optional exclude rectangle.
old-location: winmsg\calculatepopupwindowposition.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\calculatepopupwindowposition.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CalculatePopupWindowPosition, CalculatePopupWindowPosition function [Windows and Messages], TPM_BOTTOMALIGN, TPM_CENTERALIGN, TPM_HORIZONTAL, TPM_LEFTALIGN, TPM_RIGHTALIGN, TPM_TOPALIGN, TPM_VCENTERALIGN, TPM_VERTICAL, TPM_WORKAREA, _win32_CalculatePopupWindowPosition, _win32_calculatepopupwindowposition_cpp, winmsg.calculatepopupwindowposition, winui._win32_calculatepopupwindowposition, winuser/CalculatePopupWindowPosition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - CalculatePopupWindowPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CalculatePopupWindowPosition function


## -description


Calculates an appropriate pop-up window position using the specified anchor point, pop-up window size, flags, and the optional exclude rectangle. When the specified pop-up window size is smaller than the desktop window size, use the <b>CalculatePopupWindowPosition</b> function to ensure that the pop-up window is fully visible on the desktop window, regardless of the specified anchor point.


## -parameters




### -param anchorPoint [in]

Type: <b>const POINT*</b>

The specified anchor point.


### -param windowSize [in]

Type: <b>const SIZE*</b>

The specified window size.


### -param flags [in]

Type: <b>UINT</b>

Use one of the following flags to specify how the function positions the pop-up window horizontally and vertically. The flags are the same as the vertical and horizontal positioning flags of the <a href="https://msdn.microsoft.com/86b8f21b-0dfe-462e-a34a-c80ee5c1d185">TrackPopupMenuEx</a> function.


Use one of the following flags to specify how the function positions the pop-up window horizontally. 
					



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TPM_CENTERALIGN"></a><a id="tpm_centeralign"></a><dl>
<dt><b>TPM_CENTERALIGN</b></dt>
<dt>0x0004L</dt>
</dl>
</td>
<td width="60%">
Centers pop-up window horizontally relative to the coordinate specified by the anchorPoint-&gt;x parameter. 
						

</td>
</tr>
<tr>
<td width="40%"><a id="TPM_LEFTALIGN"></a><a id="tpm_leftalign"></a><dl>
<dt><b>TPM_LEFTALIGN</b></dt>
<dt>0x0000L</dt>
</dl>
</td>
<td width="60%">
Positions the pop-up window so 
						that its left edge is aligned with the coordinate specified by 
						the anchorPoint-&gt;x parameter. 
						

</td>
</tr>
<tr>
<td width="40%"><a id="TPM_RIGHTALIGN"></a><a id="tpm_rightalign"></a><dl>
<dt><b>TPM_RIGHTALIGN</b></dt>
<dt>0x0008L</dt>
</dl>
</td>
<td width="60%">
Positions the pop-up window so that its right edge is aligned with the coordinate specified by the anchorPoint-&gt;x parameter.
						

</td>
</tr>
</table>
 


Uses one of the following flags to specify how the function positions the pop-up window vertically. 
					



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TPM_BOTTOMALIGN"></a><a id="tpm_bottomalign"></a><dl>
<dt><b>TPM_BOTTOMALIGN</b></dt>
<dt>0x0020L</dt>
</dl>
</td>
<td width="60%">
Positions the pop-up window so 
					that its bottom edge is aligned with the coordinate specified by 
					the anchorPoint-&gt;y parameter. 
						

</td>
</tr>
<tr>
<td width="40%"><a id="TPM_TOPALIGN"></a><a id="tpm_topalign"></a><dl>
<dt><b>TPM_TOPALIGN</b></dt>
<dt>0x0000L</dt>
</dl>
</td>
<td width="60%">
Positions the pop-up window so 
						that its top edge is aligned with the coordinate specified by 
						the anchorPoint-&gt;y parameter. 
						

</td>
</tr>
<tr>
<td width="40%"><a id="TPM_VCENTERALIGN"></a><a id="tpm_vcenteralign"></a><dl>
<dt><b>TPM_VCENTERALIGN</b></dt>
<dt>0x0010L</dt>
</dl>
</td>
<td width="60%">
Centers the pop-up window vertically relative to the coordinate specified by the anchorPoint-&gt;y 
						parameter.
						

</td>
</tr>
</table>
 


Use one of the following flags to specify whether to accommodate horizontal or vertical alignment. 
					



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TPM_HORIZONTAL"></a><a id="tpm_horizontal"></a><dl>
<dt><b>TPM_HORIZONTAL</b></dt>
<dt>0x0000L</dt>
</dl>
</td>
<td width="60%">
If the pop-up window cannot be shown at the specified location without overlapping 
					the excluded rectangle, the system tries to accommodate the requested 
					horizontal alignment before the requested vertical alignment. 
						

</td>
</tr>
<tr>
<td width="40%"><a id="TPM_VERTICAL"></a><a id="tpm_vertical"></a><dl>
<dt><b>TPM_VERTICAL</b></dt>
<dt>0x0040L</dt>
</dl>
</td>
<td width="60%">
If the pop-up window cannot be shown at the specified location without overlapping 
					the excluded rectangle, the system tries to accommodate the requested vertical 
					alignment before the requested horizontal alignment.
						

</td>
</tr>
</table>
 


The following flag
					is available starting with Windows 7.
					



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TPM_WORKAREA"></a><a id="tpm_workarea"></a><dl>
<dt><b>TPM_WORKAREA</b></dt>
<dt>0x10000L</dt>
</dl>
</td>
<td width="60%">
Restricts the pop-up window 
						to within the work area. If this flag is not set, 
						the pop-up window is restricted to the work area only if the 
						input point is within the work area. 
						For more information, see the <b>rcWork</b> 
						and <b>rcMonitor</b> members of the <a href="https://msdn.microsoft.com/ca8ec86f-69ba-4cf8-a867-67182a3d630d">MONITORINFO</a> structure.
						

</td>
</tr>
</table>
 


### -param excludeRect [in, optional]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to a structure that specifies the exclude rectangle. 
				It can be <b>NULL</b>.


### -param popupWindowPosition [out]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to a structure that specifies the pop-up window position.
				


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, it returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>. 
				To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<b>TPM_WORKAREA</b> is supported for the <a href="https://msdn.microsoft.com/2e1e4648-e3fd-4d9a-a558-de7b030e3d75">TrackPopupMenu</a> and <a href="https://msdn.microsoft.com/86b8f21b-0dfe-462e-a34a-c80ee5c1d185">TrackPopupMenuEx</a> functions.
		 





## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/2e1e4648-e3fd-4d9a-a558-de7b030e3d75">TrackPopupMenu</a>



<a href="https://msdn.microsoft.com/86b8f21b-0dfe-462e-a34a-c80ee5c1d185">TrackPopupMenuEx</a>
 

 

