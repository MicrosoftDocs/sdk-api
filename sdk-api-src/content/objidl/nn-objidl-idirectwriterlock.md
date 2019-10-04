---
UID: NN:objidl.IDirectWriterLock
title: IDirectWriterLock (objidl.h)
author: windows-sdk-content
description: The IDirectWriterLock interface enables a single writer to obtain exclusive write access to a root storage object opened in direct mode while allowing concurrent access by multiple readers.
old-location: stg\idirectwriterlock.htm
tech.root: Stg
ms.assetid: cff56e4f-b8c5-4d87-9289-f8f2212d7c42
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectWriterLock, IDirectWriterLock interface [Structured Storage], IDirectWriterLock interface [Structured Storage],described, _stg_idirectwriterlock, objidl/IDirectWriterLock, stg.idirectwriterlock
ms.topic: interface
f1_keywords: 
 - "objidl/IDirectWriterLock"
dev_langs:
 - c++
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IDirectWriterLock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectWriterLock interface


## -description


The 
<b>IDirectWriterLock</b> interface enables a single writer to obtain exclusive write access to a root storage object opened in direct mode while allowing concurrent access by multiple readers. This single-writer, multiple-reader mode does not require the overhead of making a snapshot copy of the storage for the readers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectWriterLock</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectWriterLock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectWriterLock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-idirectwriterlock-havewriteaccess">HaveWriteAccess</a>
</td>
<td align="left" width="63%">
Indicates whether the write lock has been taken.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-idirectwriterlock-releasewriteaccess">ReleaseWriteAccess</a>
</td>
<td align="left" width="63%">
Releases the write lock previously obtained.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-idirectwriterlock-waitforwriteaccess">WaitForWriteAccess</a>
</td>
<td align="left" width="63%">
Obtains exclusive write access to a storage.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile">StgCreateDocfile</a>
 

 

