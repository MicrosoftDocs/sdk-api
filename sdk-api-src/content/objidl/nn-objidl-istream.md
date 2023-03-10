---
UID: NN:objidl.IStream
title: IStream (objidl.h)
description: The IStream interface lets you read and write data to stream objects.
helpviewer_keywords: ["IStream","IStream interface [Structured Storage]","IStream interface [Structured Storage]","described","_stg_istream","objidl/IStream","stg.istream"]
old-location: stg\istream.htm
tech.root: Stg
ms.assetid: c6f60e37-eadc-46a1-94f6-cacc23613531
ms.date: 12/05/2018
ms.keywords: IStream, IStream interface [Structured Storage], IStream interface [Structured Storage],described, _stg_istream, objidl/IStream, stg.istream
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStream
 - objidl/IStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IStream
---

# IStream interface


## -description

The 
<b>IStream</b> interface lets you read and write data to stream objects. Stream objects contain the data in a structured storage object, where storages provide the structure. Simple data can be written directly to a stream but, most frequently, streams are elements nested within a storage object. They are similar to standard files.

The 
<b>IStream</b> interface defines methods similar to the MS-DOS FAT file functions. For example, each stream object has its own access rights and a seek pointer. The main difference between a DOS file and a stream object is that in the latter case, streams are opened using an 
<b>IStream</b> interface pointer rather than a file handle.

The methods in this interface present your object's data as a contiguous sequence of bytes that you can read or write. There are also methods for committing and reverting changes on streams that are open in transacted mode and methods for restricting access to a range of bytes in the stream.

Streams can remain open for long periods of time without consuming file-system resources. The <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method is similar to a close function on a file. Once released, the stream object is no longer valid and cannot be used.

Clients of asynchronous monikers can choose between a data-pull or data-push model for driving an asynchronous 
<a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtostorage">IMoniker::BindToStorage</a> operation and for receiving asynchronous notifications. See 
<a href="/windows/desktop/com/url-monikers">URL Monikers</a> for more information. The following table compares the behavior of asynchronous 
<a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a> and 
<a href="/windows/desktop/api/objidl/nf-objidl-istream-seek">IStream::Seek</a> calls returned in <a href="https://learn.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)">IBindStatusCallback::OnDataAvailable</a> in these two download models:
<table>
<tr>
<th>IStream method call</th>
<th>Behavior in data-pull model</th>
<th>Behavior in data-push model</th>
</tr>
<tr>
<td><b>Read</b> is called to read partial data (that is, not all the available data)</td>
<td>Returns S_OK. The client must continue to read all available data before returning from <a href="https://learn.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)">IBindStatusCallback::OnDataAvailable</a> or else the bind operation is blocked. (that is, read until S_FALSE or E_PENDING is returned)</td>
<td>Returns S_OK. Even if the client returns from <a href="https://learn.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)">IBindStatusCallback::OnDataAvailable</a> at this point the bind operation continues and <b>IBindStatusCallback::OnDataAvailable</b> will be called again repeatedly until the binding finishes.</td>
</tr>
<tr>
<td><b>Read</b> is called to read all the available data</td>
<td>Returns E_PENDING if the bind operation has not completed, and <a href="https://learn.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)">IBindStatusCallback::OnDataAvailable</a> will be called again when more data is available.</td>
<td>Same as data-pull model.</td>
</tr>
<tr>
<td><b>Read</b> is called to read all the available data and the bind operation is over (end of file)</td>
<td>Returns S_FALSE. There will be a subsequent call to <a href="https://learn.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)">IBindStatusCallback::OnDataAvailable</a> with the <i>grfBSC</i> flag set to BSCF_LASTDATANOTIFICATION.</td>
<td>Same as data-pull model.</td>
</tr>
<tr>
<td><b>Seek</b> is called</td>
<td><b>Seek</b> does not work in data-pull model</td>
<td><b>Seek</b> does not work in data-push model.</td>
</tr>
</table> 

For general information on this topic, see 
<a href="/windows/desktop/com/asynchronous-monikers">Asynchronous Monikers</a> and 
<a href="/windows/desktop/com/data-pull-model-vs.-data-push-model">Data-Pull-Model versus Data Push-Model</a> for more specific information. Also, see 
<a href="/windows/desktop/com/managing-memory-allocation">Managing Memory Allocation</a> for details on COM's rules for managing memory.

## -inheritance

The <b>IStream</b> interface inherits from the <a href="/windows/win32/api/objidl/nn-objidl-isequentialstream">ISequentialStream</a> interface. <b>IStream</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-isequentialstream">ISequentialStream</a>



<a href="/windows/desktop/Stg/istream-compound-file-implementation">IStream - Compound File Implementation</a>
