---
UID: NN:shobjidl_core.IFileSystemBindData2
title: IFileSystemBindData2 (shobjidl_core.h)
description: Extends IFileSystemBindData, which stores file system information for optimizing calls to IShellFolder::ParseDisplayName. This interface adds the ability set or get file ID or junction class identifier (CLSID).
helpviewer_keywords: ["IFileSystemBindData2","IFileSystemBindData2 interface [Windows Shell]","IFileSystemBindData2 interface [Windows Shell]","described","_shell_IFileSystemBindData2","shell.IFileSystemBindData2","shobjidl_core/IFileSystemBindData2"]
old-location: shell\IFileSystemBindData2.htm
tech.root: shell
ms.assetid: c9659147-e2b6-4040-b939-42b7efec32d7
ms.date: 12/05/2018
ms.keywords: IFileSystemBindData2, IFileSystemBindData2 interface [Windows Shell], IFileSystemBindData2 interface [Windows Shell],described, _shell_IFileSystemBindData2, shell.IFileSystemBindData2, shobjidl_core/IFileSystemBindData2
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileSystemBindData2
 - shobjidl_core/IFileSystemBindData2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileSystemBindData2
---

# IFileSystemBindData2 interface


## -description

Extends <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata">IFileSystemBindData</a>, which stores file system information for optimizing calls to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a>. This interface adds the ability set or get file ID or junction class identifier (CLSID).

## -inheritance

The <b>IFileSystemBindData2</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata">IFileSystemBindData</a>. <b>IFileSystemBindData2</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata">IFileSystemBindData</a> interface, from which it inherits.

To pass the information expressed in this interface to a data source <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a>, an <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> object is created (use <a href="/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a>) and populated with an object that implements <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata">IFileSystemBindData</a> by calling the following:
  


```cpp
IBindCtx::RegisterObjectParam(STR_FILE_SYS_BIND_DATA, pfsbd)

```


 Where <i>pfsbd</i> is the object that implements <b>IFileSystemBindData</b>.

Implementers of <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a> first make the following call.
              


```cpp
IUnknown *punk;
pbc->GetObjectParam(STR_FILE_SYS_BIND_DATA, &punk);

```


 Next the implementer calls one of the <b>Get</b> methods listed above to retrieve the parameters.
