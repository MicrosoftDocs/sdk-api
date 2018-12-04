---
UID: NF:mfidl.IMFByteStreamHandler.BeginCreateObject
title: IMFByteStreamHandler::BeginCreateObject
author: windows-sdk-content
description: Begins an asynchronous request to create a media source from a byte stream.
old-location: mf\imfbytestreamhandler_begincreateobject.htm
tech.root: medfound
ms.assetid: 31dffadd-4a5a-4306-80e9-9002782f092c
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: 31dffadd-4a5a-4306-80e9-9002782f092c, BeginCreateObject, BeginCreateObject method [Media Foundation], BeginCreateObject method [Media Foundation],IMFByteStreamHandler interface, IMFByteStreamHandler interface [Media Foundation],BeginCreateObject method, IMFByteStreamHandler.BeginCreateObject, IMFByteStreamHandler::BeginCreateObject, mf.imfbytestreamhandler_begincreateobject, mfidl/IMFByteStreamHandler::BeginCreateObject
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
 - IMFByteStreamHandler.BeginCreateObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFByteStreamHandler::BeginCreateObject


## -description



Begins an asynchronous request to create a media source from a byte stream.




## -parameters




### -param pByteStream [in]

Pointer to the byte stream's <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface.


### -param pwszURL [in]

String that contains the original URL of the byte stream. This parameter can be <b>NULL</b>.


### -param dwFlags [in]

Bitwise OR of zero or more flags. See <a href="https://msdn.microsoft.com/fe0b9090-5d2a-41a4-a806-57c874d3b3a2">Source Resolver Flags</a>.


### -param pProps [in]

Pointer to the <b>IPropertyStore</b> interface of a property store. The byte-stream handler can use this property store to configure the object. This parameter can be <b>NULL</b>. For more information, see <a href="https://msdn.microsoft.com/1378bbe6-be94-4be1-b428-5ec58dabd1fa">Configuring a Media Source</a>.


### -param ppIUnknownCancelCookie [out]

Receives an <b>IUnknown</b> pointer or the value <b>NULL</b>. If the value is not <b>NULL</b>, you can cancel the asynchronous operation by passing this pointer to the <a href="https://msdn.microsoft.com/9731dac4-879c-4cbc-97b4-fa596b20c033">IMFByteStreamHandler::CancelObjectCreation</a> method. The caller must release the interface. This parameter can be <b>NULL</b>.


### -param pCallback [in]

Pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.


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



The <i>dwFlags</i> parameter must contain the MF_RESOLUTION_MEDIASOURCE flag and should not contain the MF_RESOLUTION_BYTESTREAM flag.

The byte-stream handler is responsible for parsing the stream and validating the contents. If the stream is not valid or the byte stream handler cannot parse the stream, the handler should return a failure code. The byte stream is not guaranteed to match the type of stream that the byte handler is designed to parse.

If the <i>pwszURL</i> parameter is not <b>NULL</b>, the byte-stream handler might use the URL during the resolution process. (For example, it might use the file name extension, if present.) Also, the byte stream might contain the <a href="https://msdn.microsoft.com/bcf86ece-2673-4ed8-98fd-cd0e2154b4a8">MF_BYTESTREAM_CONTENT_TYPE</a> attribute, specifying the MIME type.

When the operation completes, the byte-stream handler calls the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method. The <b>Invoke</b> method should call <a href="https://msdn.microsoft.com/8fd9797a-8dfb-4e59-8bcb-52dc53b5bb2e">IMFByteStreamHandler::EndCreateObject</a> to get a pointer to the media source.




## -see-also




<a href="https://msdn.microsoft.com/80c402d4-8246-42ee-a981-69c8d605cb0f">IMFByteStreamHandler</a>



<a href="https://msdn.microsoft.com/b0113527-f22c-4519-b1cf-fea54bff4090">Scheme Handlers and Byte-Stream Handlers</a>
 

 

