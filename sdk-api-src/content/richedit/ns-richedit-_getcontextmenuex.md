---
UID: NS:richedit._getcontextmenuex
title: "_getcontextmenuex"
author: windows-sdk-content
description: Contains context menu information that is passed to the IRichEditOleCallback::GetContextMenu method.
old-location: controls\getcontextmenuex.htm
tech.root: controls
ms.assetid: 6354921F-3C9F-4CBD-AC48-1EB67D1FDEB7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GCMF_GRIPPER, GCMF_MOUSEMENU, GCMF_SPELLING, GCMF_TOUCHMENU, GETCONTEXTMENUEX, GETCONTEXTMENUEX structure [Windows Controls], _getcontextmenuex, controls.getcontextmenuex, richedit/GETCONTEXTMENUEX
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: richedit.h
req.include-header: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - GETCONTEXTMENUEX
product: Windows
targetos: Windows
req.typenames: GETCONTEXTMENUEX
req.redist: 
---

# _getcontextmenuex structure


## -description


Contains context menu information that is passed to the <a href="https://msdn.microsoft.com/en-us/library/Bb774317(v=VS.85).aspx">IRichEditOleCallback::GetContextMenu</a> method.


## -struct-fields




### -field chrg

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb787885(v=VS.85).aspx">CHARRANGE</a></b>

The character-position range in the active display. 



### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

One or more of the following content menu flags: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GCMF_GRIPPER"></a><a id="gcmf_gripper"></a><dl>
<dt><b>GCMF_GRIPPER</b></dt>
</dl>
</td>
<td width="60%">
Get the context menu that is invoked by tapping a touch gripper handle. 


</td>
</tr>
<tr>
<td width="40%"><a id="GCMF_SPELLING"></a><a id="gcmf_spelling"></a><dl>
<dt><b>GCMF_SPELLING</b></dt>
</dl>
</td>
<td width="60%">
Get the context menu for a spelling error. 


</td>
</tr>
<tr>
<td width="40%"><a id="GCMF_MOUSEMENU"></a><a id="gcmf_mousemenu"></a><dl>
<dt><b>GCMF_MOUSEMENU</b></dt>
</dl>
</td>
<td width="60%">
Get the context menu that is invoked by mouse.

</td>
</tr>
<tr>
<td width="40%"><a id="GCMF_TOUCHMENU"></a><a id="gcmf_touchmenu"></a><dl>
<dt><b>GCMF_TOUCHMENU</b></dt>
</dl>
</td>
<td width="60%">
Get the context menu that is invoked by touch. 


</td>
</tr>
</table>
 


### -field pt

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

The screen coordinates for the content menu. 


### -field pvReserved

Type: <b>void*</b>

Not used; must be zero.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb774317(v=VS.85).aspx">IRichEditOleCallback::GetContextMenu</a>
 

 

