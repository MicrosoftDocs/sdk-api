---
UID: NF:mfidl.IMFSourceResolver.BeginCreateObjectFromURL
title: IMFSourceResolver::BeginCreateObjectFromURL (mfidl.h)
author: windows-sdk-content
description: Begins an asynchronous request to create a media source or a byte stream from a URL.
old-location: mf\imfsourceresolver_begincreateobjectfromurl.htm
tech.root: medfound
ms.assetid: bc97c1fb-d23a-4887-b6ac-0751c254a405
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BeginCreateObjectFromURL, BeginCreateObjectFromURL method [Media Foundation], BeginCreateObjectFromURL method [Media Foundation],IMFSourceResolver interface, IMFSourceResolver interface [Media Foundation],BeginCreateObjectFromURL method, IMFSourceResolver.BeginCreateObjectFromURL, IMFSourceResolver::BeginCreateObjectFromURL, bc97c1fb-d23a-4887-b6ac-0751c254a405, mf.imfsourceresolver_begincreateobjectfromurl, mfidl/IMFSourceResolver::BeginCreateObjectFromURL
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
 - IMFSourceResolver.BeginCreateObjectFromURL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSourceResolver::BeginCreateObjectFromURL


## -description



Begins an asynchronous request to create a media source or a byte stream from a URL.




## -parameters




### -param pwszURL [in]

Null-terminated string that contains the URL to resolve.


### -param dwFlags [in]

Bitwise OR of flags. See <a href="https://msdn.microsoft.com/fe0b9090-5d2a-41a4-a806-57c874d3b3a2">Source Resolver Flags</a>.


### -param pProps [in]

Pointer to the <b>IPropertyStore</b> interface of a property store. The method passes the property store to the scheme handler or byte-stream handler that creates the object. The handler can use the property store to configure the object. This parameter can be <b>NULL</b>. For more information, see <a href="https://msdn.microsoft.com/1378bbe6-be94-4be1-b428-5ec58dabd1fa">Configuring a Media Source</a>.


### -param ppIUnknownCancelCookie [out]

Receives an <b>IUnknown</b> pointer or the value <b>NULL</b>. If the value is not <b>NULL</b>, you can cancel the asynchronous operation by passing this pointer to the <a href="https://msdn.microsoft.com/6a30ac92-a281-4293-8975-987fa25a5318">IMFSourceResolver::CancelObjectCreation</a> method. The caller must release the interface. This parameter can be <b>NULL</b>.


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
<dt><b>MF_E_SOURCERESOLVER_MUTUALLY_EXCLUSIVE_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter contains mutually exclusive flags.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_SCHEME</b></dt>
</dl>
</td>
<td width="60%">
The URL scheme is not supported.

</td>
</tr>
</table>
 




## -remarks



The <i>dwFlags</i> parameter must contain either the MF_RESOLUTION_MEDIASOURCE flag or the MF_RESOLUTION_BYTESTREAM flag, but should not contain both.

For local files, you can pass the file name in the <i>pwszURL</i> parameter; the <code>file:</code> scheme is not required.

When the operation completes, the source resolver calls the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method. The <b>Invoke</b> method should call <a href="https://msdn.microsoft.com/af50a76d-b083-4815-bbff-820b21ff8d1b">IMFSourceResolver::EndCreateObjectFromURL</a> to get a pointer to the object that was created.

The usage of the <i>pProps</i> parameter depends on the implementation of the media source. 




## -see-also




<a href="https://msdn.microsoft.com/079c61c5-7a29-4411-840e-9349190726ac">IMFSourceResolver</a>



<a href="https://msdn.microsoft.com/93eecf10-308b-4bb4-92f9-fd32d6ecdb04">Source Resolver</a>
 

 

