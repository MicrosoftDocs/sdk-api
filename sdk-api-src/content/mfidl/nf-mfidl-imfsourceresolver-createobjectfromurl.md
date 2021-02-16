---
UID: NF:mfidl.IMFSourceResolver.CreateObjectFromURL
title: IMFSourceResolver::CreateObjectFromURL (mfidl.h)
description: Creates a media source or a byte stream from a URL. This method is synchronous.
helpviewer_keywords: ["CreateObjectFromURL","CreateObjectFromURL method [Media Foundation]","CreateObjectFromURL method [Media Foundation]","IMFSourceResolver interface","IMFSourceResolver interface [Media Foundation]","CreateObjectFromURL method","IMFSourceResolver.CreateObjectFromURL","IMFSourceResolver::CreateObjectFromURL","b8f751b1-6456-4d67-839d-ecfa388e8d71","mf.imfsourceresolver_createobjectfromurl","mfidl/IMFSourceResolver::CreateObjectFromURL"]
old-location: mf\imfsourceresolver_createobjectfromurl.htm
tech.root: mf
ms.assetid: b8f751b1-6456-4d67-839d-ecfa388e8d71
ms.date: 12/05/2018
ms.keywords: CreateObjectFromURL, CreateObjectFromURL method [Media Foundation], CreateObjectFromURL method [Media Foundation],IMFSourceResolver interface, IMFSourceResolver interface [Media Foundation],CreateObjectFromURL method, IMFSourceResolver.CreateObjectFromURL, IMFSourceResolver::CreateObjectFromURL, b8f751b1-6456-4d67-839d-ecfa388e8d71, mf.imfsourceresolver_createobjectfromurl, mfidl/IMFSourceResolver::CreateObjectFromURL
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSourceResolver::CreateObjectFromURL
 - mfidl/IMFSourceResolver::CreateObjectFromURL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSourceResolver.CreateObjectFromURL
---

# IMFSourceResolver::CreateObjectFromURL


## -description

Creates a media source or a byte stream from a URL. This method is synchronous.

## -parameters

### -param pwszURL [in]

Null-terminated string that contains the URL to resolve.

### -param dwFlags [in]

Bitwise OR of one or more flags. See <a href="/windows/desktop/medfound/source-resolver-flags">Source Resolver Flags</a>.
          See remarks below.

### -param pProps [in]

Pointer to the <b>IPropertyStore</b> interface of a property store. The method passes the property store to the scheme handler or byte-stream handler that creates the object. The handler can use the property store to configure the object. This parameter can be <b>NULL</b>. For more information, see <a href="/windows/desktop/medfound/configuring-a-media-source">Configuring a Media Source</a>.

### -param pObjectType [out]

Receives a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mf_object_type">MF_OBJECT_TYPE</a> enumeration, specifying the type of object that was created.

### -param ppObject [out]

Receives a pointer to the object's <b>IUnknown</b> interface. The caller must release the interface.

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

The <i>dwFlags</i> parameter must contain either the <b>MF_RESOLUTION_MEDIASOURCE</b> flag or the <b>MF_RESOLUTION_BYTESTREAM</b> flag, but should not contain both.

It is recommended that you do not set <b>MF_RESOLUTION_WRITE</b> on the input argument <i>dwFlags</i>  unless it is necessary for your scenario. For most use-cases, media sources do not need to be created with write capability. Creating a media source with write capability may have a lower probability of success than creating a media source without write capability. This is because there can be stricter checks on the content represented by the URL when creating a media source with write capability.

For local files, you can pass the file name in the <i>pwszURL</i> parameter; the <code>file:</code> scheme is not required.

<div class="alert"><b>Note</b>  This method cannot be called remotely.</div>
<div> </div>

#### Examples


```cpp
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver">IMFSourceResolver</a>



<a href="/windows/desktop/medfound/source-resolver">Source Resolver</a>