---
UID: NF:mfidl.IMFSourceResolver.CreateObjectFromByteStream
title: IMFSourceResolver::CreateObjectFromByteStream
author: windows-sdk-content
description: Creates a media source from a byte stream. This method is synchronous.
old-location: mf\imfsourceresolver_createobjectfrombytestream.htm
old-project: medfound
ms.assetid: e4a4aad5-0924-4251-b0da-6919ae010bf0
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: CreateObjectFromByteStream, CreateObjectFromByteStream method [Media Foundation], CreateObjectFromByteStream method [Media Foundation],IMFSourceResolver interface, IMFSourceResolver interface [Media Foundation],CreateObjectFromByteStream method, IMFSourceResolver.CreateObjectFromByteStream, IMFSourceResolver::CreateObjectFromByteStream, e4a4aad5-0924-4251-b0da-6919ae010bf0, mf.imfsourceresolver_createobjectfrombytestream, mfidl/IMFSourceResolver::CreateObjectFromByteStream
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
 - IMFSourceResolver.CreateObjectFromByteStream
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSourceResolver::CreateObjectFromByteStream


## -description


Creates a media source from a byte stream. This method is synchronous.
        


## -parameters




### -param pByteStream [in]

Pointer to the byte stream's <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface.
          


### -param pwszURL [in]

Null-terminated string that contains the URL of the byte stream. The URL is optional and can be <b>NULL</b>. See Remarks for more information.
          


### -param dwFlags [in]

Bitwise <b>OR</b> of flags. See <a href="https://msdn.microsoft.com/fe0b9090-5d2a-41a4-a806-57c874d3b3a2">Source Resolver Flags</a>.
          


### -param pProps [in]

Pointer to the <b>IPropertyStore</b> interface of a property store. The method passes the property store to the byte-stream handler. The byte-stream handler can use the property store to configure the media source. This parameter can be <b>NULL</b>. For more information, see <a href="https://msdn.microsoft.com/1378bbe6-be94-4be1-b428-5ec58dabd1fa">Configuring a Media Source</a>.
          


### -param pObjectType [out]

Receives a member of the <a href="https://msdn.microsoft.com/e919ae78-e3a5-42c5-b4e0-186e7e4fe54a">MF_OBJECT_TYPE</a> enumeration, specifying the type of object that was created.
          


### -param ppObject [out]

Receives a pointer to the media source's <b>IUnknown</b> interface. The caller must release the interface.
          


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
<dt><b>MF_E_UNSUPPORTED_BYTESTREAM_TYPE</b></dt>
</dl>
</td>
<td width="60%">
This byte stream is not supported.
              

</td>
</tr>
</table>
 




## -remarks



The <i>dwFlags</i> parameter must contain the <b>MF_RESOLUTION_MEDIASOURCE</b> flag and should not contain the <b>MF_RESOLUTION_BYTESTREAM</b> flag.

The source resolver attempts to find one or more byte-stream handlers for the byte stream, based on the file name extension of the URL, or the MIME type of the byte stream (or both). The URL is specified in the optional <i>pwszURL</i> parameter, and the MIME type may be specified in the <a href="https://msdn.microsoft.com/bcf86ece-2673-4ed8-98fd-cd0e2154b4a8">MF_BYTESTREAM_CONTENT_TYPE</a> attribute on the byte stream. Byte-stream handlers are registered by file name extension or MIME type, or both, as described in <a href="https://msdn.microsoft.com/b0113527-f22c-4519-b1cf-fea54bff4090">Scheme Handlers and Byte-Stream Handlers</a>. The caller should specify at least one of these values (both if possible):

<ul>
<li>Specify the URL in the <i>pwszURL</i> parameter.
          </li>
<li>Specify the MIME type by setting the <a href="https://msdn.microsoft.com/bcf86ece-2673-4ed8-98fd-cd0e2154b4a8">MF_BYTESTREAM_CONTENT_TYPE</a> attribute on the byte stream. (This attribute might be set already when you create the byte stream, depending on how the byte stream was created.)
          </li>
</ul>
<div class="alert"><b>Note</b>  This method cannot be called remotely.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/079c61c5-7a29-4411-840e-9349190726ac">IMFSourceResolver</a>



<a href="https://msdn.microsoft.com/93eecf10-308b-4bb4-92f9-fd32d6ecdb04">Source Resolver</a>
 

 

