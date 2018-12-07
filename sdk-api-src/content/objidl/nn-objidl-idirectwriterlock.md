---
UID: NN:objidl.IDirectWriterLock
title: IDirectWriterLock
author: windows-sdk-content
description: The IDirectWriterLock interface enables a single writer to obtain exclusive write access to a root storage object opened in direct mode while allowing concurrent access by multiple readers.
old-location: stg\idirectwriterlock.htm
tech.root: stg
ms.assetid: cff56e4f-b8c5-4d87-9289-f8f2212d7c42
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirectWriterLock, IDirectWriterLock interface [Structured Storage], IDirectWriterLock interface [Structured Storage],described, _stg_idirectwriterlock, objidl/IDirectWriterLock, stg.idirectwriterlock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectWriterLock interface


## -description


The 
<b>IDirectWriterLock</b> interface enables a single writer to obtain exclusive write access to a root storage object opened in direct mode while allowing concurrent access by multiple readers. This single-writer, multiple-reader mode does not require the overhead of making a snapshot copy of the storage for the readers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectWriterLock</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectWriterLock</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8366b6b5-73c3-4b05-be68-c24ecd2eab96">HaveWriteAccess</a>
</td>
<td align="left" width="63%">
Indicates whether the write lock has been taken.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/849eeb79-60fd-4345-9e04-2ed7a7ede5ca">ReleaseWriteAccess</a>
</td>
<td align="left" width="63%">
Releases the write lock previously obtained.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4505bed-325b-494e-93bd-7bf23b3a1215">WaitForWriteAccess</a>
</td>
<td align="left" width="63%">
Obtains exclusive write access to a storage.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>



<a href="https://msdn.microsoft.com/3292484b-8eff-438d-b989-b58ae323872b">StgCreateDocfile</a>
 

 

