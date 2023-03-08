---
UID: NS:richedit._getcontextmenuex
title: GETCONTEXTMENUEX (richedit.h)
description: Contains context menu information that is passed to the IRichEditOleCallback::GetContextMenu method.
helpviewer_keywords: ["GCMF_GRIPPER","GCMF_MOUSEMENU","GCMF_SPELLING","GCMF_TOUCHMENU","GETCONTEXTMENUEX","GETCONTEXTMENUEX structure [Windows Controls]","controls.getcontextmenuex","richedit/GETCONTEXTMENUEX"]
old-location: controls\getcontextmenuex.htm
tech.root: Controls
ms.assetid: 6354921F-3C9F-4CBD-AC48-1EB67D1FDEB7
ms.date: 12/05/2018
ms.keywords: GCMF_GRIPPER, GCMF_MOUSEMENU, GCMF_SPELLING, GCMF_TOUCHMENU, GETCONTEXTMENUEX, GETCONTEXTMENUEX structure [Windows Controls], controls.getcontextmenuex, richedit/GETCONTEXTMENUEX
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
targetos: Windows
req.typenames: GETCONTEXTMENUEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _getcontextmenuex
 - richedit/_getcontextmenuex
 - GETCONTEXTMENUEX
 - richedit/GETCONTEXTMENUEX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - GETCONTEXTMENUEX
---

# GETCONTEXTMENUEX structure


## -description

Contains context menu information that is passed to the <a href="/windows/win32/api/richole/nf-richole-iricheditolecallback-getcontextmenu">IRichEditOleCallback::GetContextMenu</a> method.

## -struct-fields

### -field chrg

Type: <b><a href="/windows/win32/api/richedit/ns-richedit-charrange">CHARRANGE</a></b>

The character-position range in the active display.

### -field dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

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

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The screen coordinates for the content menu.

### -field pvReserved

Type: <b>void*</b>

Not used; must be zero.

## -see-also

<a href="/windows/win32/api/richole/nf-richole-iricheditolecallback-getcontextmenu">IRichEditOleCallback::GetContextMenu</a>
