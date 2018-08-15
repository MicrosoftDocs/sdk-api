---
UID: NF:mfidl.IMFByteStreamHandler.CancelObjectCreation
title: IMFByteStreamHandler::CancelObjectCreation
author: windows-sdk-content
description: Cancels the current request to create a media source.
old-location: mf\imfbytestreamhandler_cancelobjectcreation.htm
old-project: medfound
ms.assetid: 9731dac4-879c-4cbc-97b4-fa596b20c033
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 9731dac4-879c-4cbc-97b4-fa596b20c033, CancelObjectCreation, CancelObjectCreation method [Media Foundation], CancelObjectCreation method [Media Foundation],IMFByteStreamHandler interface, IMFByteStreamHandler interface [Media Foundation],CancelObjectCreation method, IMFByteStreamHandler.CancelObjectCreation, IMFByteStreamHandler::CancelObjectCreation, mf.imfbytestreamhandler_cancelobjectcreation, mfidl/IMFByteStreamHandler::CancelObjectCreation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFByteStreamHandler.CancelObjectCreation
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFByteStreamHandler::CancelObjectCreation


## -description



Cancels the current request to create a media source.




## -parameters




### -param pIUnknownCancelCookie [in]

Pointer to the <b>IUnknown</b> interface that was returned in the <i>ppIUnknownCancelCookie</i> parameter of the <a href="https://msdn.microsoft.com/31dffadd-4a5a-4306-80e9-9002782f092c">IMFByteStreamHandler::BeginCreateObject</a> method.


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



You can use this method to cancel a previous call to <a href="https://msdn.microsoft.com/31dffadd-4a5a-4306-80e9-9002782f092c">BeginCreateObject</a>. Because that method is asynchronous, however, it might be completed before the operation can be canceled. Therefore, your callback might still be invoked after you call this method.




## -see-also




<a href="https://msdn.microsoft.com/80c402d4-8246-42ee-a981-69c8d605cb0f">IMFByteStreamHandler</a>



<a href="https://msdn.microsoft.com/b0113527-f22c-4519-b1cf-fea54bff4090">Scheme Handlers and Byte-Stream Handlers</a>
 

 

