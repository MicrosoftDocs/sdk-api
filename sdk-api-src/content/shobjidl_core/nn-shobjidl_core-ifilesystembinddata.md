---
UID: NN:shobjidl_core.IFileSystemBindData
title: IFileSystemBindData (shobjidl_core.h)
description: Exposes methods that store file system information for optimizing calls to IShellFolder::ParseDisplayName.
helpviewer_keywords: ["IFileSystemBindData","IFileSystemBindData interface [Windows Shell]","IFileSystemBindData interface [Windows Shell]","described","_shell_ifilesystembinddata","shell.IFileSystemBindData","shobjidl_core/IFileSystemBindData"]
old-location: shell\IFileSystemBindData.htm
tech.root: shell
ms.assetid: f5099bb3-21a7-4708-ac48-d32a14646614
ms.date: 12/05/2018
ms.keywords: IFileSystemBindData, IFileSystemBindData interface [Windows Shell], IFileSystemBindData interface [Windows Shell],described, _shell_ifilesystembinddata, shell.IFileSystemBindData, shobjidl_core/IFileSystemBindData
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileSystemBindData
 - shobjidl_core/IFileSystemBindData
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
 - IFileSystemBindData
---

# IFileSystemBindData interface


## -description

Exposes methods that store file system information for optimizing calls to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a>.

## -inheritance

The <b>IFileSystemBindData</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFileSystemBindData</b> also has these types of members:

## -remarks

<b>IFileSystemBindData</b> stores the file system information in a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure. The object that implements <b>IFileSystemBindData</b> is then stored in a bind context that is passed to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a>.

Implement <b>IFileSystemBindData</b> when you want to optimize calls to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a> and you already have the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure's file information available to you.

To store the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> information prior to calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a>, the client uses the following procedure.

<ol>
<li>Create an instance of the object that exposes the <b>IFileSystemBindData</b> interface.</li>
<li>Use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesystembinddata-setfinddata">IFileSystemBindData::SetFindData</a> to store the data in the object.</li>
<li>Store the object in a bind context through the <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam">IBindCtx::RegisterObjectParam</a> method. Set the <i>pszKey</i> parameter to the string <code>L"File System Bind Data"</code> and the <i>punk</i> parameter to the address of the <b>IFileSystemBindData</b> interface.</li>
</ol>
The bind context is then passed with the call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a>.

<div class="alert"><b>Note</b>  Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>
