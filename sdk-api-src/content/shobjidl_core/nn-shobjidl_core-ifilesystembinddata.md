---
UID: NN:shobjidl_core.IFileSystemBindData
title: IFileSystemBindData (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that store file system information for optimizing calls to IShellFolder::ParseDisplayName.
old-location: shell\IFileSystemBindData.htm
tech.root: shell
ms.assetid: f5099bb3-21a7-4708-ac48-d32a14646614
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFileSystemBindData, IFileSystemBindData interface [Windows Shell], IFileSystemBindData interface [Windows Shell],described, _shell_ifilesystembinddata, shell.IFileSystemBindData, shobjidl_core/IFileSystemBindData
ms.topic: interface
f1_keywords:
- shobjidl_core/IFileSystemBindData
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IFileSystemBindData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileSystemBindData interface


## -description


Exposes methods that store file system information for optimizing calls to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSystemBindData</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFileSystemBindData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileSystemBindData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesystembinddata-getfinddata">GetFindData</a>
</td>
<td align="left" width="63%">
Gets the file system information stored in the <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesystembinddata-setfinddata">SetFindData</a>
</td>
<td align="left" width="63%">
Stores file system information in a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure. This information is used by <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a>.

</td>
</tr>
</table> 


## -remarks



<b>IFileSystemBindData</b> stores the file system information in a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure. The object that implements <b>IFileSystemBindData</b> is then stored in a bind context that is passed to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a>.

Implement <b>IFileSystemBindData</b> when you want to optimize calls to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a> and you already have the <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure's file information available to you.

To store the <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> information prior to calling <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a>, the client uses the following procedure.

<ol>
<li>Create an instance of the object that exposes the <b>IFileSystemBindData</b> interface.</li>
<li>Use <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesystembinddata-setfinddata">IFileSystemBindData::SetFindData</a> to store the data in the object.</li>
<li>Store the object in a bind context through the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam">IBindCtx::RegisterObjectParam</a> method. Set the <i>pszKey</i> parameter to the string <code>L"File System Bind Data"</code> and the <i>punk</i> parameter to the address of the <b>IFileSystemBindData</b> interface.</li>
</ol>
The bind context is then passed with the call to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a>.

<div class="alert"><b>Note</b>  Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>


