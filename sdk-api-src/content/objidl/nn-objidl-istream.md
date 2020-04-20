---
UID: NN:objidl.IStream
title: IStream (objidl.h)
description: The IStream interface lets you read and write data to stream objects.helpviewer_keywords: ["IStream","IStream interface [Structured Storage]","IStream interface [Structured Storage]","described","_stg_istream","objidl/IStream","stg.istream"]
old-location: stg\istream.htm
tech.root: Stg
ms.assetid: c6f60e37-eadc-46a1-94f6-cacc23613531
ms.date: 12/05/2018
ms.keywords: IStream, IStream interface [Structured Storage], IStream interface [Structured Storage],described, _stg_istream, objidl/IStream, stg.istream
f1_keywords:
- objidl/IStream
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
- IStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStream interface


## -description


The 
<b>IStream</b> interface lets you read and write data to stream objects. Stream objects contain the data in a structured storage object, where storages provide the structure. Simple data can be written directly to a stream but, most frequently, streams are elements nested within a storage object. They are similar to standard files.

The 
<b>IStream</b> interface defines methods similar to the MS-DOS FAT file functions. For example, each stream object has its own access rights and a seek pointer. The main difference between a DOS file and a stream object is that in the latter case, streams are opened using an 
<b>IStream</b> interface pointer rather than a file handle.

The methods in this interface present your object's data as a contiguous sequence of bytes that you can read or write. There are also methods for committing and reverting changes on streams that are open in transacted mode and methods for restricting access to a range of bytes in the stream.

Streams can remain open for long periods of time without consuming file-system resources. The <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method is similar to a close function on a file. Once released, the stream object is no longer valid and cannot be used.

Clients of asynchronous monikers can choose between a data-pull or data-push model for driving an asynchronous 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imoniker-bindtostorage">IMoniker::BindToStorage</a> operation and for receiving asynchronous notifications. See 
<a href="https://docs.microsoft.com/windows/desktop/com/url-monikers">URL Monikers</a> for more information. The following table compares the behavior of asynchronous 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-seek">IStream::Seek</a> calls returned in <a href="https://msdn.microsoft.com/9755eda0-4d33-49e1-9bdd-f50a906e826f">IBindStatusCallback::OnDataAvailable</a> in these two download models:
<table>
<tr>
<th>IStream method call</th>
<th>Behavior in data-pull model</th>
<th>Behavior in data-push model</th>
</tr>
<tr>
<td><b>Read</b> is called to read partial data (that is, not all the available data)</td>
<td>Returns S_OK. The client must continue to read all available data before returning from <a href="https://msdn.microsoft.com/9755eda0-4d33-49e1-9bdd-f50a906e826f">IBindStatusCallback::OnDataAvailable</a> or else the bind operation is blocked. (that is, read until S_FALSE or E_PENDING is returned)</td>
<td>Returns S_OK. Even if the client returns from <a href="https://msdn.microsoft.com/9755eda0-4d33-49e1-9bdd-f50a906e826f">IBindStatusCallback::OnDataAvailable</a> at this point the bind operation continues and <b>IBindStatusCallback::OnDataAvailable</b> will be called again repeatedly until the binding finishes.</td>
</tr>
<tr>
<td><b>Read</b> is called to read all the available data</td>
<td>Returns E_PENDING if the bind operation has not completed, and <a href="https://msdn.microsoft.com/9755eda0-4d33-49e1-9bdd-f50a906e826f">IBindStatusCallback::OnDataAvailable</a> will be called again when more data is available.</td>
<td>Same as data-pull model.</td>
</tr>
<tr>
<td><b>Read</b> is called to read all the available data and the bind operation is over (end of file)</td>
<td>Returns S_FALSE. There will be a subsequent call to <a href="https://msdn.microsoft.com/9755eda0-4d33-49e1-9bdd-f50a906e826f">IBindStatusCallback::OnDataAvailable</a> with the <i>grfBSC</i> flag set to BSCF_LASTDATANOTIFICATION.</td>
<td>Same as data-pull model.</td>
</tr>
<tr>
<td><b>Seek</b> is called</td>
<td><b>Seek</b> does not work in data-pull model</td>
<td><b>Seek</b> does not work in data-push model.</td>
</tr>
</table> 

For general information on this topic, see 
<a href="https://docs.microsoft.com/windows/desktop/com/asynchronous-monikers">Asynchronous Monikers</a> and 
<a href="https://docs.microsoft.com/windows/desktop/com/data-pull-model-vs.-data-push-model">Data-Pull-Model versus Data Push-Model</a> for more specific information. Also, see 
<a href="https://docs.microsoft.com/windows/desktop/com/managing-memory-allocation">Managing Memory Allocation</a> for details on COM's rules for managing memory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStream</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new stream object that references the same bytes as the original stream but provides a separate seek pointer to those bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-commit">Commit</a>
</td>
<td align="left" width="63%">
Ensures that any changes made to a stream object open in transacted mode are reflected in the parent storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-copyto">CopyTo</a>
</td>
<td align="left" width="63%">
Copies a specified number of bytes from the current seek pointer in the stream to the current seek pointer in another stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-lockregion">LockRegion</a>
</td>
<td align="left" width="63%">
Restricts access to a specified range of bytes in the stream. Supporting this functionality is optional since some file systems do not provide it.

</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">Read</a>
</td>
<td align="left" width="63%">
Reads a specified number of bytes from the stream object into memory starting at the current seek pointer.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-isequentialstream">ISequentialStream</a>)</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-revert">Revert</a>
</td>
<td align="left" width="63%">
Discards all changes that have been made to a transacted stream since the last call to 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-commit">IStream::Commit</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-seek">Seek</a>
</td>
<td align="left" width="63%">
Changes the seek pointer to a new location relative to the beginning of the stream, the end of the stream, or the current seek pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-setsize">SetSize</a>
</td>
<td align="left" width="63%">
Changes the size of the stream object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-stat">Stat</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure for this stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-unlockregion">UnlockRegion</a>
</td>
<td align="left" width="63%">
Removes the access restriction on a range of bytes previously restricted with 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-lockregion">IStream::LockRegion</a>.

</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">Write</a>
</td>
<td align="left" width="63%">
Writes a specified number of bytes into the stream object starting at the current seek pointer.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-isequentialstream">ISequentialStream</a>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-isequentialstream">ISequentialStream</a>



<a href="https://docs.microsoft.com/windows/desktop/Stg/istream-compound-file-implementation">IStream - Compound File Implementation</a>
 

 

