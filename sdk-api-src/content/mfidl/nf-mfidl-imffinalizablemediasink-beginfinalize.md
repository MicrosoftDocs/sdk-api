---
UID: NF:mfidl.IMFFinalizableMediaSink.BeginFinalize
title: IMFFinalizableMediaSink::BeginFinalize (mfidl.h)
author: windows-sdk-content
description: Notifies the media sink to asynchronously take any steps it needs to finish its tasks.
old-location: mf\imffinalizablemediasink_beginfinalize.htm
tech.root: medfound
ms.assetid: fbcb7722-ba64-40a6-9c43-26a6b8dce7f6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BeginFinalize, BeginFinalize method [Media Foundation], BeginFinalize method [Media Foundation],IMFFinalizableMediaSink interface, IMFFinalizableMediaSink interface [Media Foundation],BeginFinalize method, IMFFinalizableMediaSink.BeginFinalize, IMFFinalizableMediaSink::BeginFinalize, fbcb7722-ba64-40a6-9c43-26a6b8dce7f6, mf.imffinalizablemediasink_beginfinalize, mfidl/IMFFinalizableMediaSink::BeginFinalize
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFFinalizableMediaSink.BeginFinalize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFFinalizableMediaSink::BeginFinalize


## -description



Notifies the media sink to asynchronously take any steps it needs to finish its tasks.




## -parameters




### -param pCallback [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of an asynchronous object. The caller must implement this interface.


### -param punkState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



Many archive media sinks have steps they need to do at the end of archiving to complete their file operations, such as updating the header (for some formats) or flushing all pending writes to disk. In some cases, this may include expensive operations such as indexing the content. <b>BeginFinalize</b> is an asynchronous way to initiate final tasks.

When the finalize operation is complete, the callback object's <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method is called. At that point, the application should call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imffinalizablemediasink-endfinalize">IMFFinalizableMediaSink::EndFinalize</a> to complete the asynchronous request.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink">IMFFinalizableMediaSink</a>
 

 

