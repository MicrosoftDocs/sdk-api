---
UID: NN:shobjidl_core.IDefaultFolderMenuInitialize
title: IDefaultFolderMenuInitialize (shobjidl_core.h)
author: windows-sdk-content
description: Provides methods used to get and set shortcut menu information. This information is the same as that provided to SHCreateDefaultContextMenu through the DEFCONTEXTMENU structure.
old-location: shell\IDefaultFolderMenuInitialize.htm
tech.root: shell
ms.assetid: 23C75435-E43D-4451-8F03-AE051BC1B66D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDefaultFolderMenuInitialize, IDefaultFolderMenuInitialize interface [Windows Shell], IDefaultFolderMenuInitialize interface [Windows Shell],described, shell.IDefaultFolderMenuInitialize, shobjidl_core/IDefaultFolderMenuInitialize
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IDefaultFolderMenuInitialize"
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IDefaultFolderMenuInitialize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDefaultFolderMenuInitialize interface


## -description


Provides methods used to get and set shortcut menu information. This information is the same as that provided to <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu">SHCreateDefaultContextMenu</a> through the <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu">DEFCONTEXTMENU</a> structure.
<div class="alert"><b>Note</b>  Do not use this method to reinitialize a shortcut menu; use <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize">IShellExtInit::Initialize</a> instead.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDefaultFolderMenuInitialize</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDefaultFolderMenuInitialize</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDefaultFolderMenuInitialize</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idefaultfoldermenuinitialize-getmenurestrictions">GetMenuRestrictions</a>
</td>
<td align="left" width="63%"></td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idefaultfoldermenuinitialize-initialize">Initialize</a>
</td>
<td align="left" width="63%"></td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idefaultfoldermenuinitialize-sethandlerclsid">SetHandlerClsid</a>
</td>
<td align="left" width="63%"></td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idefaultfoldermenuinitialize-setmenurestrictions">SetMenuRestrictions</a>
</td>
<td align="left" width="63%"></td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

