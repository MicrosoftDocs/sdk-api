---
UID: NF:immdev.ImmAssociateContextEx
title: ImmAssociateContextEx function (immdev.h)
description: The ImmAssociateContextEx function (immdev.h) changes the association between the input method context and the specified window or its children.
helpviewer_keywords: ["IACE_CHILDREN","IACE_DEFAULT","IACE_IGNORENOCONTEXT","ImmAssociateContextEx","ImmAssociateContextEx function [Internationalization for Windows Applications]","_win32_ImmAssociateContextEx","imm/ImmAssociateContextEx","intl.immassociatecontextex"]
old-location: intl\immassociatecontextex.htm
tech.root: Intl
ms.assetid: 7f44d274-b5e9-4feb-acd6-5c68b3f7d868
ms.date: 08/04/2022
ms.keywords: IACE_CHILDREN, IACE_DEFAULT, IACE_IGNORENOCONTEXT, ImmAssociateContextEx, ImmAssociateContextEx function [Internationalization for Windows Applications], _win32_ImmAssociateContextEx, imm/ImmAssociateContextEx, intl.immassociatecontextex
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
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
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImmAssociateContextEx
 - immdev/ImmAssociateContextEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-imm-l1-1-2.dll
 - imm32.dll
 - Ext-MS-Win-imm-l1-1-0.dll
 - ext-ms-win-imm-l1-1-1.dll
api_name:
 - ImmAssociateContextEx
---

# ImmAssociateContextEx function


## -description

Changes the association between the input method context and the specified window or its children.

## -parameters

### -param unnamedParam1 [in]

Handle to the window to associate with the input context.

### -param unnamedParam2 [in]

Handle to the input method context.

### -param unnamedParam3 [in]

Flags specifying the type of association between the window and the input method context. This parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IACE_CHILDREN"></a><a id="iace_children"></a><dl>
<dt><b>IACE_CHILDREN</b></dt>
</dl>
</td>
<td width="60%">
Associate the input method context to the child windows of the specified window only.

</td>
</tr>
<tr>
<td width="40%"><a id="IACE_DEFAULT"></a><a id="iace_default"></a><dl>
<dt><b>IACE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Restore the default input method context of the window.

</td>
</tr>
<tr>
<td width="40%"><a id="IACE_IGNORENOCONTEXT"></a><a id="iace_ignorenocontext"></a><dl>
<dt><b>IACE_IGNORENOCONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Do not associate the input method context with windows that are not associated with any input method context.

</td>
</tr>
</table>

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.

## -remarks

If the application calls this function with IACE_CHILDREN, the operating system associates the specified input method context with child windows of the window indicated by <i>hWnd</i>. It associates the input method context only with child windows of the thread that creates <i>hWnd</i>. Any child window that is created after this function has been called will not be affected. Instead, the default input method context will be associated with it.

If the application calls this function with IACE_DEFAULT, the operating system restores the default input method context for the window. In this case, the <i>hIMC</i> parameter is ignored.

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
