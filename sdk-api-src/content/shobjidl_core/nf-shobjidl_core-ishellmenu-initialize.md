---
UID: NF:shobjidl_core.IShellMenu.Initialize
title: IShellMenu::Initialize (shobjidl_core.h)
description: Initializes a menu band.
helpviewer_keywords: ["IShellMenu interface [Windows Shell]","Initialize method","IShellMenu.Initialize","IShellMenu::Initialize","Initialize","Initialize method [Windows Shell]","Initialize method [Windows Shell]","IShellMenu interface","SMINIT_CACHED","SMINIT_DEFAULT","SMINIT_HORIZONTAL","SMINIT_RESTRICT_DRAGDROP","SMINIT_TOPLEVEL","SMINIT_VERTICAL","_shell_IShellMenu_Initialize","shell.IShellMenu_Initialize","shobjidl_core/IShellMenu::Initialize"]
old-location: shell\IShellMenu_Initialize.htm
tech.root: shell
ms.assetid: dc9864df-21f3-4b0b-b862-48055032c071
ms.date: 12/05/2018
ms.keywords: IShellMenu interface [Windows Shell],Initialize method, IShellMenu.Initialize, IShellMenu::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IShellMenu interface, SMINIT_CACHED, SMINIT_DEFAULT, SMINIT_HORIZONTAL, SMINIT_RESTRICT_DRAGDROP, SMINIT_TOPLEVEL, SMINIT_VERTICAL, _shell_IShellMenu_Initialize, shell.IShellMenu_Initialize, shobjidl_core/IShellMenu::Initialize
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellMenu::Initialize
 - shobjidl_core/IShellMenu::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellMenu.Initialize
---

# IShellMenu::Initialize


## -description

Initializes a menu band.

## -parameters

### -param psmc [in, optional]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback">IShellMenuCallback</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback">IShellMenuCallback</a> interface. This interface receives notifications from the menu. This value can be <b>NULL</b>.

### -param uId [in]

Type: <b>UINT</b>

The identifier of the selected menu item. Set this parameter to -1 for the menu itself.

### -param uIdAncestor [in]

Type: <b>UINT</b>

### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that control how the menu operates.


A combination of the following option values:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SMINIT_DEFAULT"></a><a id="sminit_default"></a><dl>
<dt><b>SMINIT_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
No options.

</td>
</tr>
<tr>
<td width="40%"><a id="SMINIT_RESTRICT_DRAGDROP"></a><a id="sminit_restrict_dragdrop"></a><dl>
<dt><b>SMINIT_RESTRICT_DRAGDROP</b></dt>
</dl>
</td>
<td width="60%">
Do not allow drag-and-drop.

</td>
</tr>
<tr>
<td width="40%"><a id="SMINIT_TOPLEVEL"></a><a id="sminit_toplevel"></a><dl>
<dt><b>SMINIT_TOPLEVEL</b></dt>
</dl>
</td>
<td width="60%">
This is the top band.

</td>
</tr>
<tr>
<td width="40%"><a id="SMINIT_CACHED"></a><a id="sminit_cached"></a><dl>
<dt><b>SMINIT_CACHED</b></dt>
</dl>
</td>
<td width="60%">
Do not destroy the band when the window is closed.

</td>
</tr>
</table>
 


In addition to the values above, one of the following layout options:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SMINIT_VERTICAL"></a><a id="sminit_vertical"></a><dl>
<dt><b>SMINIT_VERTICAL</b></dt>
</dl>
</td>
<td width="60%">
Specifies a vertical band.

</td>
</tr>
<tr>
<td width="40%"><a id="SMINIT_HORIZONTAL"></a><a id="sminit_horizontal"></a><dl>
<dt><b>SMINIT_HORIZONTAL</b></dt>
</dl>
</td>
<td width="60%">
Specifies a horizontal band.

</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.