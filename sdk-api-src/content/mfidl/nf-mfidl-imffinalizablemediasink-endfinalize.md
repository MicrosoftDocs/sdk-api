---
UID: NF:mfidl.IMFFinalizableMediaSink.EndFinalize
title: IMFFinalizableMediaSink::EndFinalize
author: windows-sdk-content
description: Completes an asynchronous finalize operation.
old-location: mf\imffinalizablemediasink_endfinalize.htm
tech.root: medfound
ms.assetid: 1b2a9b24-69da-41c7-8379-3f3d066d2582
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: 1b2a9b24-69da-41c7-8379-3f3d066d2582, EndFinalize, EndFinalize method [Media Foundation], EndFinalize method [Media Foundation],IMFFinalizableMediaSink interface, IMFFinalizableMediaSink interface [Media Foundation],EndFinalize method, IMFFinalizableMediaSink.EndFinalize, IMFFinalizableMediaSink::EndFinalize, mf.imffinalizablemediasink_endfinalize, mfidl/IMFFinalizableMediaSink::EndFinalize
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
 - IMFFinalizableMediaSink.EndFinalize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFFinalizableMediaSink::EndFinalize


## -description



Completes an asynchronous finalize operation.




## -parameters




### -param pResult [in]

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method.


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



Call this method after the <a href="https://msdn.microsoft.com/fbcb7722-ba64-40a6-9c43-26a6b8dce7f6">IMFFinalizableMediaSink::BeginFinalize</a> method completes asynchronously.




## -see-also




<a href="https://msdn.microsoft.com/e60c2773-f2fc-469e-a698-036390cbed16">IMFFinalizableMediaSink</a>
 

 

