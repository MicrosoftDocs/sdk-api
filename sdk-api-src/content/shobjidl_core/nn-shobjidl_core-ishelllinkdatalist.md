---
UID: NN:shobjidl_core.IShellLinkDataList
title: IShellLinkDataList (shobjidl_core.h)
description: Exposes methods that allow an application to attach extra data blocks to a Shell link. These methods add, copy, or remove data blocks.
helpviewer_keywords: ["IShellLinkDataList","IShellLinkDataList interface [Windows Shell]","IShellLinkDataList interface [Windows Shell]","described","_win32_IShellLinkDataList","shell.IShellLinkDataList","shobjidl_core/IShellLinkDataList"]
old-location: shell\IShellLinkDataList.htm
tech.root: shell
ms.assetid: ac3279ad-1413-48bf-a830-4ec128352573
ms.date: 12/05/2018
ms.keywords: IShellLinkDataList, IShellLinkDataList interface [Windows Shell], IShellLinkDataList interface [Windows Shell],described, _win32_IShellLinkDataList, shell.IShellLinkDataList, shobjidl_core/IShellLinkDataList
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellLinkDataList
 - shobjidl_core/IShellLinkDataList
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
 - IShellLinkDataList
---

# IShellLinkDataList interface


## -description

Exposes methods that allow an application to attach extra data blocks to a <a href="/windows/desktop/shell/links">Shell link</a>. These methods add, copy, or remove data blocks.

## -inheritance

The <b>IShellLinkDataList</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellLinkDataList</b> also has these types of members:

## -remarks

The data blocks are in the form of a structure. The first two members are the same for all data blocks. The first member gives the structure's size. The second member is a signature that identifies the type of data block. The remaining members hold the block's data. There are five types of data block currently supported.
				


<table class="clsStd">
<tr>
<th>Data block structure</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_darwin_link">EXP_DARWIN_LINK</a>
</td>
<td>The link's Windows Installer ID.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_special_folder">EXP_SPECIAL_FOLDER</a>
</td>
<td>Special folder information.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_sz_link">EXP_SZ_LINK</a>
</td>
<td>The target name.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_console_props">NT_CONSOLE_PROPS</a>
</td>
<td>Console properties.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_fe_console_props">NT_FE_CONSOLE_PROPS</a>
</td>
<td>The console's code page.</td>
</tr>
</table>
 



This interface is not implemented by applications.

Use this interface if your application needs to add extra data blocks to a Shell link.

<div class="alert"><b>Note</b>  <b>Windows Vista and later.</b> Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>
