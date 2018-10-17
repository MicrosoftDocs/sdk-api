---
UID: NF:mfmediaengine.IMFMediaEngineExtension.BeginCreateObject
title: IMFMediaEngineExtension::BeginCreateObject
author: windows-sdk-content
description: Begins an asynchronous request to create either a byte stream or a media source.
old-location: mf\imfmediaengineextension_begincreateobject.htm
tech.root: medfound
ms.assetid: 804E9F16-E4C9-41F6-8913-950A569FB835
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: BeginCreateObject, BeginCreateObject method [Media Foundation], BeginCreateObject method [Media Foundation],IMFMediaEngineExtension interface, IMFMediaEngineExtension interface [Media Foundation],BeginCreateObject method, IMFMediaEngineExtension.BeginCreateObject, IMFMediaEngineExtension::BeginCreateObject, MF_OBJECT_BYTESTREAM, MF_OBJECT_MEDIASOURCE, mf.imfmediaengineextension_begincreateobject, mfmediaengine/IMFMediaEngineExtension::BeginCreateObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineExtension.BeginCreateObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineExtension::BeginCreateObject


## -description


Begins an asynchronous request to create either a byte stream or a media source.


## -parameters




### -param bstrURL [in]

The URL of the media resource.


### -param pByteStream [in]

A pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface.

If the <i>type</i> parameter equals  <b>MF_OBJECT_BYTESTREAM</b>, this parameter is <b>NULL</b>. 

If <i>type</i> equals <b>MF_OBJECT_MEDIASOURCE</b>, this parameter either contains a pointer to a byte stream or is <b>NULL</b>. See Remarks for more information.


### -param type [in]

A member of the <a href="https://msdn.microsoft.com/e919ae78-e3a5-42c5-b4e0-186e7e4fe54a">MF_OBJECT_TYPE</a> enumeration that specifies which type of object to create.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_OBJECT_BYTESTREAM"></a><a id="mf_object_bytestream"></a><dl>
<dt><b>MF_OBJECT_BYTESTREAM</b></dt>
</dl>
</td>
<td width="60%">
Create a byte stream. The byte stream must support the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_OBJECT_MEDIASOURCE"></a><a id="mf_object_mediasource"></a><dl>
<dt><b>MF_OBJECT_MEDIASOURCE</b></dt>
</dl>
</td>
<td width="60%">
Create a media source. The media source must support the <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> interface.

</td>
</tr>
</table>
 


### -param ppIUnknownCancelCookie [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.  This pointer can be used to cancel the asynchronous operation, by passing the pointer to the <a href="https://msdn.microsoft.com/E2FEC865-221E-41B5-8271-32A53D60619E">IMFMediaEngineExtension::CancelObjectCreation</a> method. 

The caller must release the interface. This parameter can be NULL.


### -param pCallback [in]

A pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface. This interface is used to signal the completion of the asynchronous operation.


### -param punkState [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of an object impemented by the caller. You can use this object to hold state information for the callback. The object is returned to the caller when the callback is invoked. This parameter can be <b>NULL</b>. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method requests the object to create either a byte stream or a media source, depending on the value of the <i>type</i> parameter:

<ul>
<li>If <i>type</i> is <b>MF_OBJECT_BYTESTREAM</b>, the method creates a byte stream for the URL that is specified in <i>bstrURL</i>. In this case, the <i>pByteStream</i> parameter is <b>NULL</b>. </li>
<li>If <i>type</i> is <b>MF_OBJECT_MEDIASOURCE</b>, the method creates a media source, using the byte stream that is specified in the <i>pByteStream</i> parameter. Note that <i>pByteStream</i> can also be <b>NULL</b> in this case.</li>
</ul>
The method is performed asynchronously. The Media Engine calls the <a href="https://msdn.microsoft.com/F2B19870-7529-4C8C-9FE6-B312F6A2D2ED">IMFMediaEngineExtension::EndCreateObject</a> method to complete the operation.

<h3><a id="Implemention_Notes"></a><a id="implemention_notes"></a><a id="IMPLEMENTION_NOTES"></a>Implemention Notes</h3>
A Media Engine extension can be used to support a custom byte stream object, a custom media source, or both. For a byte stream, create the byte stream object when <i>type</i> equals <b>MF_OBJECT_BYTESTREAM</b>. For a media source, create the source when the type equals <b>MF_OBJECT_MEDIASOURCE</b>.

To load a URL, the Media Engine performs the following steps:<ol>
<li>Try to create a byte stream from the URL.</li>
<li>If a byte stream is successfully created, try to create a media source from the byte stream.</li>
<li>If a byte stream cannot be created, try to create a media source directly from the URL.</li>
</ol>


At each step, the Media Engine calls <b>IMFMediaEngineExtension::BeginCreateObject</b> on the extension object. If the <b>BeginCreateObject</b> method fails, the Media Engine tries the <a href="https://msdn.microsoft.com/93eecf10-308b-4bb4-92f9-fd32d6ecdb04">Source Resolver</a>.

In your <b>BeginCreateObject</b> method, you can choose to handle any of the following cases:<ul>
<li>The <i>type</i> parameter is <b>MF_OBJECT_BYTESTREAM</b>. Create a byte stream from the URL.</li>
<li>The <i>type</i> parameter is <b>MF_OBJECT_MEDIASOURCE</b> and <i>pByteStream</i> points to a byte stream. Use the byte stream to create a media source. </li>
<li>The <i>type</i> parameter is <b>MF_OBJECT_MEDIASOURCE</b> and <i>pByteStream</i> is <b>NULL</b>. Create a media source from the URL.</li>
</ul>


Return a failure code for any cases that you do not handle. 

Examples:<ul>
<li>To support a custom media format, implement a media source. If the media source does not require any special byte-stream implementation, create the media source when <i>type</i> is <b>MF_OBJECT_MEDIASOURCE</b> and <i>pByteStream</i> is non-<b>NULL</b>. The standard Microsoft Media Foundation byte stream implementation will be used in this case.</li>
<li>To support a custom URL scheme, handle the case where <i>type</i> is <b>MF_OBJECT_BYTESTREAM</b> and return a byte stream object that is capable of reading the URL. </li>
</ul>


If the <b>BeginCreateObject</b> method succeeds, the operation should be performed asynchronously. When the operation completes, call the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method on the callback interface specified in <i>pCallback</i>. The Media Engine completes the operation by calling <a href="https://msdn.microsoft.com/F2B19870-7529-4C8C-9FE6-B312F6A2D2ED">IMFMediaEngineExtension::EndCreateObject</a>.




## -see-also




<a href="https://msdn.microsoft.com/A032E0D0-2201-4B81-9FE0-8E9CE2707FDB">IMFMediaEngineExtension</a>
 

 

