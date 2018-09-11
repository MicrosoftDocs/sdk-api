---
UID: NF:mfidl.IMFByteStreamHandler.GetMaxNumberOfBytesRequiredForResolution
title: IMFByteStreamHandler::GetMaxNumberOfBytesRequiredForResolution
author: windows-sdk-content
description: Retrieves the maximum number of bytes needed to create the media source or determine that the byte stream handler cannot parse this stream.
old-location: mf\imfbytestreamhandler_getmaxnumberofbytesrequiredforresolution.htm
tech.root: medfound
ms.assetid: e90c5bc6-fc0a-4478-aa65-9dc6618f46f0
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetMaxNumberOfBytesRequiredForResolution, GetMaxNumberOfBytesRequiredForResolution method [Media Foundation], GetMaxNumberOfBytesRequiredForResolution method [Media Foundation],IMFByteStreamHandler interface, IMFByteStreamHandler interface [Media Foundation],GetMaxNumberOfBytesRequiredForResolution method, IMFByteStreamHandler.GetMaxNumberOfBytesRequiredForResolution, IMFByteStreamHandler::GetMaxNumberOfBytesRequiredForResolution, e90c5bc6-fc0a-4478-aa65-9dc6618f46f0, mf.imfbytestreamhandler_getmaxnumberofbytesrequiredforresolution, mfidl/IMFByteStreamHandler::GetMaxNumberOfBytesRequiredForResolution
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
 - IMFByteStreamHandler.GetMaxNumberOfBytesRequiredForResolution
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFByteStreamHandler::GetMaxNumberOfBytesRequiredForResolution


## -description



Retrieves the maximum number of bytes needed to create the media source or determine that the byte stream handler cannot parse this stream.




## -parameters




### -param pqwBytes [out]

Receives the maximum number of bytes that are required.


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
 




## -see-also




<a href="https://msdn.microsoft.com/80c402d4-8246-42ee-a981-69c8d605cb0f">IMFByteStreamHandler</a>



<a href="https://msdn.microsoft.com/b0113527-f22c-4519-b1cf-fea54bff4090">Scheme Handlers and Byte-Stream Handlers</a>
 

 

