---
UID: NS:commctrl._tagEDITBALLOONTIP
title: "_tagEDITBALLOONTIP"
author: windows-sdk-content
description: Contains information about a balloon tip associated with a button control.
old-location: controls\EDITBALLOONTIP.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolstructures\editballoontip.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PEDITBALLOONTIP, EDITBALLOONTIP, EDITBALLOONTIP structure [Windows Controls], PEDITBALLOONTIP, PEDITBALLOONTIP structure pointer [Windows Controls], TTI_ERROR, TTI_ERROR_LARGE, TTI_INFO, TTI_INFO_LARGE, TTI_NONE, TTI_WARNING, TTI_WARNING_LARGE, _tagEDITBALLOONTIP, _win32_EDITBALLOONTIP_str, _win32_EDITBALLOONTIP_str_cpp, commctrl/EDITBALLOONTIP, commctrl/PEDITBALLOONTIP, controls.EDITBALLOONTIP, controls._win32_EDITBALLOONTIP_str"
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - EDITBALLOONTIP
product: Windows
targetos: Windows
req.typenames: EDITBALLOONTIP, *PEDITBALLOONTIP
req.redist: 
---

# _tagEDITBALLOONTIP structure


## -description


Contains information about a balloon tip associated with a button control.


## -struct-fields




### -field cbStruct

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A <b>DWORD</b> that contains the size, in bytes, of the structure. 


### -field pszTitle

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

A pointer to a Unicode string that contains the title of the balloon tip. 


### -field pszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

A pointer to a Unicode string that contains the balloon tip text. 


### -field ttiIcon

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

A value of type <b>INT</b> that specifies the type of icon to associate with the balloon tip. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TTI_ERROR"></a><a id="tti_error"></a><dl>
<dt><b>TTI_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Use the error icon.

</td>
</tr>
<tr>
<td width="40%"><a id="TTI_INFO"></a><a id="tti_info"></a><dl>
<dt><b>TTI_INFO</b></dt>
</dl>
</td>
<td width="60%">
Use the information icon.

</td>
</tr>
<tr>
<td width="40%"><a id="TTI_NONE"></a><a id="tti_none"></a><dl>
<dt><b>TTI_NONE</b></dt>
</dl>
</td>
<td width="60%">
Use no icon.

</td>
</tr>
<tr>
<td width="40%"><a id="TTI_WARNING"></a><a id="tti_warning"></a><dl>
<dt><b>TTI_WARNING</b></dt>
</dl>
</td>
<td width="60%">
Use the warning icon.

</td>
</tr>
<tr>
<td width="40%"><a id="TTI_INFO_LARGE"></a><a id="tti_info_large"></a><dl>
<dt><b>TTI_INFO_LARGE</b></dt>
</dl>
</td>
<td width="60%">
Use the large information icon. This is assumed to be an HICON value.

</td>
</tr>
<tr>
<td width="40%"><a id="TTI_WARNING_LARGE"></a><a id="tti_warning_large"></a><dl>
<dt><b>TTI_WARNING_LARGE</b></dt>
</dl>
</td>
<td width="60%">
Use the large warning icon. This is assumed to be an HICON value.

</td>
</tr>
<tr>
<td width="40%"><a id="TTI_ERROR_LARGE"></a><a id="tti_error_large"></a><dl>
<dt><b>TTI_ERROR_LARGE</b></dt>
</dl>
</td>
<td width="60%">
Use the large error icon. This is assumed to be an HICON value.

</td>
</tr>
</table>
 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/1e6915b7-4b61-43b2-be13-b89c72378a1a">EM_SHOWBALLOONTIP</a>



<a href="https://msdn.microsoft.com/2a71b92c-f57a-4c27-80b7-e1d9092f3701">Edit Controls</a>



<a href="https://msdn.microsoft.com/18ee941e-6919-4451-a192-c7342c72617d">Edit_ShowBalloonTip</a>



<b>Reference</b>
 

 

