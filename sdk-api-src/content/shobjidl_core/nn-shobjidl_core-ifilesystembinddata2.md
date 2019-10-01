---
UID: NN:shobjidl_core.IFileSystemBindData2
title: IFileSystemBindData2 (shobjidl_core.h)
author: windows-sdk-content
description: Extends IFileSystemBindData, which stores file system information for optimizing calls to IShellFolder::ParseDisplayName. This interface adds the ability set or get file ID or junction class identifier (CLSID).
old-location: shell\IFileSystemBindData2.htm
tech.root: shell
ms.assetid: c9659147-e2b6-4040-b939-42b7efec32d7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFileSystemBindData2, IFileSystemBindData2 interface [Windows Shell], IFileSystemBindData2 interface [Windows Shell],described, _shell_IFileSystemBindData2, shell.IFileSystemBindData2, shobjidl_core/IFileSystemBindData2
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IFileSystemBindData2"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileSystemBindData2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileSystemBindData2 interface


## -description


Extends <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata">IFileSystemBindData</a>, which stores file system information for optimizing calls to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a>. This interface adds the ability set or get file ID or junction class identifier (CLSID).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSystemBindData2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata">IFileSystemBindData</a>. <b>IFileSystemBindData2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileSystemBindData2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesystembinddata2-getfileid">GetFileID</a>
</td>
<td align="left" width="63%">
Gets the unique file identifier for the current file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesystembinddata2-getjunctionclsid">GetJunctionCLSID</a>
</td>
<td align="left" width="63%">
Gets the CLSID of the object that implements <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> for the item, if the item is a junction point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesystembinddata2-setfileid">SetFileID</a>
</td>
<td align="left" width="63%">
Sets the unique file identifier for the current file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesystembinddata2-setjunctionclsid">SetJunctionCLSID</a>
</td>
<td align="left" width="63%">
Sets the CLSID of the object that implements <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>, if the current item is a junction point.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata">IFileSystemBindData</a> interface, from which it inherits.

To pass the information expressed in this interface to a data source <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a>, an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> object is created (use <a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a>) and populated with an object that implements <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata">IFileSystemBindData</a> by calling the following:
  


```cpp
IBindCtx::RegisterObjectParam(STR_FILE_SYS_BIND_DATA, pfsbd)

```


 Where <i>pfsbd</i> is the object that implements <b>IFileSystemBindData</b>.

Implementers of <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a> first make the following call.
              


```cpp
IUnknown *punk;
pbc->GetObjectParam(STR_FILE_SYS_BIND_DATA, &punk);

```


 Next the implementer calls one of the <b>Get</b> methods listed above to retrieve the parameters.
            



