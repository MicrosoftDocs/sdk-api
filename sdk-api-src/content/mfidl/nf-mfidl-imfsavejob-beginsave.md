---
UID: NF:mfidl.IMFSaveJob.BeginSave
title: IMFSaveJob::BeginSave
author: windows-sdk-content
description: Begins saving a Windows Media file to the application's byte stream.
old-location: mf\imfsavejob_beginsave.htm
tech.root: medfound
ms.assetid: ff137b76-2a05-4e58-8d4f-d12cdd89656b
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: BeginSave, BeginSave method [Media Foundation], BeginSave method [Media Foundation],IMFSaveJob interface, IMFSaveJob interface [Media Foundation],BeginSave method, IMFSaveJob.BeginSave, IMFSaveJob::BeginSave, ff137b76-2a05-4e58-8d4f-d12cdd89656b, mf.imfsavejob_beginsave, mfidl/IMFSaveJob::BeginSave
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMFSaveJob.BeginSave
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSaveJob::BeginSave


## -description



Begins saving a Windows Media file to the application's byte stream.




## -parameters




### -param pStream [in]

Pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of the application's byte stream. The data from the source byte stream is written to this byte stream.


### -param pCallback [in]

Pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface


### -param pState [in]

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



When the operation completes, the callback object's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method is called. At that point, the application should call <a href="https://msdn.microsoft.com/9d63d7b5-4454-4301-b467-eea82bace6ff">IMFSaveJob::EndSave</a> to complete the asynchronous request.




## -see-also




<a href="https://msdn.microsoft.com/0f38fa60-ed04-40c4-9bb0-b6e196cd9586">IMFSaveJob</a>
 

 

