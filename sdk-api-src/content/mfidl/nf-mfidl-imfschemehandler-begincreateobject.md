---
UID: NF:mfidl.IMFSchemeHandler.BeginCreateObject
title: IMFSchemeHandler::BeginCreateObject
author: windows-sdk-content
description: Begins an asynchronous request to create an object from a URL.When the Source Resolver creates a media source from a URL, it passes the request to a scheme handler.
old-location: mf\imfschemehandler_begincreateobject.htm
tech.root: medfound
ms.assetid: 78858e8c-0eb3-4b62-84f0-76e9dff0e3ce
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: 78858e8c-0eb3-4b62-84f0-76e9dff0e3ce, BeginCreateObject, BeginCreateObject method [Media Foundation], BeginCreateObject method [Media Foundation],IMFSchemeHandler interface, IMFSchemeHandler interface [Media Foundation],BeginCreateObject method, IMFSchemeHandler.BeginCreateObject, IMFSchemeHandler::BeginCreateObject, mf.imfschemehandler_begincreateobject, mfidl/IMFSchemeHandler::BeginCreateObject
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
 - IMFSchemeHandler.BeginCreateObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSchemeHandler::BeginCreateObject


## -description



Begins an asynchronous request to create an object from a URL.

When the <a href="https://msdn.microsoft.com/93eecf10-308b-4bb4-92f9-fd32d6ecdb04">Source Resolver</a> creates a media source from a URL, it passes the request to a scheme handler. The scheme handler might create a media source directly from the URL, or it might return a byte stream. If it returns a byte stream, the source resolver use a byte-stream handler to create the media source from the byte stream.




## -parameters




### -param pwszURL [in]

A null-terminated string that contains the URL to resolve.
          


### -param dwFlags [in]

A bitwise <b>OR</b> of one or more flags. See <a href="https://msdn.microsoft.com/fe0b9090-5d2a-41a4-a806-57c874d3b3a2">Source Resolver Flags</a>.
          


### -param pProps [in]

A pointer to the <b>IPropertyStore</b> interface of a property store. The scheme handler can use this property store to configure the object. This parameter can be <b>NULL</b>. For more information, see <a href="https://msdn.microsoft.com/1378bbe6-be94-4be1-b428-5ec58dabd1fa">Configuring a Media Source</a>.
          


### -param ppIUnknownCancelCookie [out]

Receives an <b>IUnknown</b> pointer or the value <b>NULL</b>. If the value is not <b>NULL</b>, you can cancel the asynchronous operation by passing this pointer to the <a href="https://msdn.microsoft.com/662a4c47-95f8-4a84-ab2b-96e51d13906c">IMFSchemeHandler::CancelObjectCreation</a> method. The caller must release the interface. This parameter can be <b>NULL</b>, in which case the <b>IUnknown</b> pointer is not returned to the caller.
          


### -param pCallback [in]

A pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.
          


### -param punkState [in]

A pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.
          


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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Cannot open the URL with the requested access (read or write).
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_BYTESTREAM_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Unsupported byte stream type.
              

</td>
</tr>
</table>
 




## -remarks



The <i>dwFlags</i> parameter must contain the <b>MF_RESOLUTION_MEDIASOURCE</b> flag or the <b>MF_RESOLUTION_BYTESTREAM</b> flag. If the <b>MF_RESOLUTION_MEDIASOURCE</b> flag is set, the scheme handler might create the media source directly from the URL, or it might create a byte stream. The type of object is returned in the <i>pObjectType</i> parameter of the <a href="https://msdn.microsoft.com/e3f88904-c30f-4d40-ac79-c83b0a06f1fa">IMFSchemeHandler::EndCreateObject</a> method. If the scheme handler returns a byte stream, the source resolver will pass the byte stream to a byte-stream handler, which will create the media source from the byte stream.

If the <b>MF_RESOLUTION_BYTESTREAM</b> flag is set, the scheme handler will attempt to create a byte stream from the URL. However, if the scheme handler is designed to create a media source directly, rather than a byte stream, the method will fail.

The following table summarizes the behavior of these two flags when passed to this method:

<table>
<tr>
<th>Flag</th>
<th>Object created</th>
</tr>
<tr>
<td><b>MF_RESOLUTION_MEDIASOURCE</b></td>
<td>Media source or byte stream</td>
</tr>
<tr>
<td><b>MF_RESOLUTION_BYTESTREAM</b></td>
<td>Byte stream</td>
</tr>
</table>
 

The <b>MF_RESOLUTION_MEDIASOURCE</b> and <b>MF_RESOLUTION_BYTESTREAM</b> flags can be combined, although in this case it is redundant.

When the operation completes, the scheme handler calls the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method. The Invoke method should call <a href="https://msdn.microsoft.com/e3f88904-c30f-4d40-ac79-c83b0a06f1fa">IMFSchemeHandler::EndCreateObject</a> to get a pointer to the created object.




## -see-also




<a href="https://msdn.microsoft.com/a342054e-2cb5-494a-a2f7-d144c72d1fa5">IMFSchemeHandler</a>



<a href="https://msdn.microsoft.com/b0113527-f22c-4519-b1cf-fea54bff4090">Scheme Handlers and Byte-Stream Handlers</a>
 

 

