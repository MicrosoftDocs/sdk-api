---
UID: NS:winuser.tagMOUSEHOOKSTRUCTEX
title: tagMOUSEHOOKSTRUCTEX
author: windows-sdk-content
description: Contains information about a mouse event passed to a WH_MOUSE hook procedure, MouseProc. This is an extension of the MOUSEHOOKSTRUCT structure that includes information about wheel movement or the use of the X button.
old-location: winmsg\mousehookstructex.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookstructures\mousehookstructex.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPMOUSEHOOKSTRUCTEX, *PMOUSEHOOKSTRUCTEX, LPMOUSEHOOKSTRUCTEX, LPMOUSEHOOKSTRUCTEX structure pointer [Windows and Messages], MOUSEHOOKSTRUCTEX, MOUSEHOOKSTRUCTEX structure [Windows and Messages], PMOUSEHOOKSTRUCTEX, PMOUSEHOOKSTRUCTEX structure pointer [Windows and Messages], XBUTTON1, XBUTTON2, _win32_MOUSEHOOKSTRUCTEX_str, _win32_mousehookstructex_str_cpp, tagMOUSEHOOKSTRUCTEX, winmsg.mousehookstructex, winui._win32_mousehookstructex_str, winuser/LPMOUSEHOOKSTRUCTEX, winuser/MOUSEHOOKSTRUCTEX, winuser/PMOUSEHOOKSTRUCTEX"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MOUSEHOOKSTRUCTEX, *LPMOUSEHOOKSTRUCTEX, *PMOUSEHOOKSTRUCTEX
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - MOUSEHOOKSTRUCTEX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagMOUSEHOOKSTRUCTEX structure


## -description


Contains information about a mouse event passed to a <b>WH_MOUSE</b> hook procedure, <a href="https://msdn.microsoft.com/4fc1d81d-ee12-4ee4-b29c-2450b92b83b5">MouseProc</a>. 

This is an extension of the <a href="https://msdn.microsoft.com/e2304163-2c31-4a94-8b5e-435a7f8aa5f6">MOUSEHOOKSTRUCT</a> structure that includes information about wheel movement or the use of the X button.


## -struct-fields




### -field mouseData

Type: <b>DWORD</b>

If the message is <a href="https://msdn.microsoft.com/9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb">WM_MOUSEWHEEL</a>, the HIWORD of this member is the wheel delta. The LOWORD is undefined and reserved. A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user. One wheel click is defined as WHEEL_DELTA, which is 120. 

If the message is <a href="https://msdn.microsoft.com/4d972841-1513-4925-9d59-2557233561a2">WM_XBUTTONDOWN</a>, <a href="https://msdn.microsoft.com/ad726859-368a-4603-bffa-4e639bc69a6a">WM_XBUTTONUP</a>, <a href="https://msdn.microsoft.com/68f7abaf-cf6d-499a-957f-3c4d73cdbdee">WM_XBUTTONDBLCLK</a>, <a href="https://msdn.microsoft.com/72744c98-1898-4548-bd10-61ad53eeab15">WM_NCXBUTTONDOWN</a>, <a href="https://msdn.microsoft.com/07ab5d4e-9912-4867-9146-8abc5addc15d">WM_NCXBUTTONUP</a>, or <a href="https://msdn.microsoft.com/8c0b1e96-9cbb-4ef8-83ff-9253f1a934ef">WM_NCXBUTTONDBLCLK</a>, the HIWORD of 
						<b>mouseData</b> specifies which X button was pressed or released, and the LOWORD is undefined and reserved. This member can be one or more of the following values. Otherwise, 
						<b>mouseData</b> is not used. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XBUTTON1"></a><a id="xbutton1"></a><dl>
<dt><b>XBUTTON1</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The first X button was pressed or released.

</td>
</tr>
<tr>
<td width="40%"><a id="XBUTTON2"></a><a id="xbutton2"></a><dl>
<dt><b>XBUTTON2</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The second X button was pressed or released.

</td>
</tr>
</table>
 


### -field tagMOUSEHOOKSTRUCT

 




#### - MOUSEHOOKSTRUCT

Type: <b><a href="https://msdn.microsoft.com/e2304163-2c31-4a94-8b5e-435a7f8aa5f6">MOUSEHOOKSTRUCT</a></b>

The members of a <a href="https://msdn.microsoft.com/e2304163-2c31-4a94-8b5e-435a7f8aa5f6">MOUSEHOOKSTRUCT</a> structure make up the first part of this structure. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/987095d7-059f-4eae-925d-6723ab6d524c">Hooks</a>



<a href="https://msdn.microsoft.com/e2304163-2c31-4a94-8b5e-435a7f8aa5f6">MOUSEHOOKSTRUCT</a>



<a href="https://msdn.microsoft.com/4fc1d81d-ee12-4ee4-b29c-2450b92b83b5">MouseProc</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb">WM_MOUSEWHEEL</a>



<a href="https://msdn.microsoft.com/8c0b1e96-9cbb-4ef8-83ff-9253f1a934ef">WM_NCXBUTTONDBLCLK</a>



<a href="https://msdn.microsoft.com/72744c98-1898-4548-bd10-61ad53eeab15">WM_NCXBUTTONDOWN</a>



<a href="https://msdn.microsoft.com/07ab5d4e-9912-4867-9146-8abc5addc15d">WM_NCXBUTTONUP</a>



<a href="https://msdn.microsoft.com/68f7abaf-cf6d-499a-957f-3c4d73cdbdee">WM_XBUTTONDBLCLK</a>



<a href="https://msdn.microsoft.com/4d972841-1513-4925-9d59-2557233561a2">WM_XBUTTONDOWN</a>



<a href="https://msdn.microsoft.com/ad726859-368a-4603-bffa-4e639bc69a6a">WM_XBUTTONUP</a>
 

 

