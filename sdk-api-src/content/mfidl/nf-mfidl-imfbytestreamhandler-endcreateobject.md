---
UID: NF:mfidl.IMFByteStreamHandler.EndCreateObject
title: IMFByteStreamHandler::EndCreateObject
author: windows-sdk-content
description: Completes an asynchronous request to create a media source.
old-location: mf\imfbytestreamhandler_endcreateobject.htm
tech.root: medfound
ms.assetid: 8fd9797a-8dfb-4e59-8bcb-52dc53b5bb2e
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 8fd9797a-8dfb-4e59-8bcb-52dc53b5bb2e, EndCreateObject, EndCreateObject method [Media Foundation], EndCreateObject method [Media Foundation],IMFByteStreamHandler interface, IMFByteStreamHandler interface [Media Foundation],EndCreateObject method, IMFByteStreamHandler.EndCreateObject, IMFByteStreamHandler::EndCreateObject, mf.imfbytestreamhandler_endcreateobject, mfidl/IMFByteStreamHandler::EndCreateObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFByteStreamHandler.EndCreateObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFByteStreamHandler::EndCreateObject


## -description



Completes an asynchronous request to create a media source.




## -parameters




### -param pResult [in]

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">Invoke</a> method.


### -param pObjectType [out]

Receives a member of the <a href="https://msdn.microsoft.com/e919ae78-e3a5-42c5-b4e0-186e7e4fe54a">MF_OBJECT_TYPE</a> enumeration, specifying the type of object that was created.


### -param ppObject [out]

Receives a pointer to the <b>IUnknown</b> interface of the media source. The caller must release the interface.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The operation was canceled. See <a href="https://msdn.microsoft.com/9731dac4-879c-4cbc-97b4-fa596b20c033">IMFByteStreamHandler::CancelObjectCreation</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_CANNOT_PARSE_BYTESTREAM</b></dt>
</dl>
</td>
<td width="60%">
Unable to parse the byte stream.

</td>
</tr>
</table>
 




## -remarks



Call this method from inside the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method.




## -see-also




<a href="https://msdn.microsoft.com/80c402d4-8246-42ee-a981-69c8d605cb0f">IMFByteStreamHandler</a>



<a href="https://msdn.microsoft.com/b0113527-f22c-4519-b1cf-fea54bff4090">Scheme Handlers and Byte-Stream Handlers</a>
 

 

