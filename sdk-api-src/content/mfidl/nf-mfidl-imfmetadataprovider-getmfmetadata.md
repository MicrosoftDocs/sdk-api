---
UID: NF:mfidl.IMFMetadataProvider.GetMFMetadata
title: IMFMetadataProvider::GetMFMetadata (mfidl.h)
description: Gets a collection of metadata, either for an entire presentation, or for one stream in the presentation.
helpviewer_keywords: ["0a3c1932-c301-4ecd-b640-02d7bcfc2aca","GetMFMetadata","GetMFMetadata method [Media Foundation]","GetMFMetadata method [Media Foundation]","IMFMetadataProvider interface","IMFMetadataProvider interface [Media Foundation]","GetMFMetadata method","IMFMetadataProvider.GetMFMetadata","IMFMetadataProvider::GetMFMetadata","mf.imfmetadataprovider_getmfmetadata","mfidl/IMFMetadataProvider::GetMFMetadata"]
old-location: mf\imfmetadataprovider_getmfmetadata.htm
tech.root: mf
ms.assetid: 0a3c1932-c301-4ecd-b640-02d7bcfc2aca
ms.date: 12/05/2018
ms.keywords: 0a3c1932-c301-4ecd-b640-02d7bcfc2aca, GetMFMetadata, GetMFMetadata method [Media Foundation], GetMFMetadata method [Media Foundation],IMFMetadataProvider interface, IMFMetadataProvider interface [Media Foundation],GetMFMetadata method, IMFMetadataProvider.GetMFMetadata, IMFMetadataProvider::GetMFMetadata, mf.imfmetadataprovider_getmfmetadata, mfidl/IMFMetadataProvider::GetMFMetadata
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
 - IMFMetadataProvider::GetMFMetadata
 - mfidl/IMFMetadataProvider::GetMFMetadata
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
 - IMFMetadataProvider.GetMFMetadata
---

# IMFMetadataProvider::GetMFMetadata


## -description

Gets a collection of metadata, either for an entire presentation, or for one stream in the presentation.

## -parameters

### -param pPresentationDescriptor [in]

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor">IMFPresentationDescriptor</a> interface of the media source's presentation descriptor.

### -param dwStreamIdentifier [in]

If this parameter is zero, the method retrieves metadata that applies to the entire presentation. Otherwise, this <i></i> parameter specifies a stream identifier, and the method retrieves metadata for that stream. To get the stream identifier for a stream, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier">IMFStreamDescriptor::GetStreamIdentifier</a>.

### -param dwFlags [in]

Reserved. Must be zero.

### -param ppMFMetadata [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadata">IMFMetadata</a> interface. Use this interface to access the metadata. The caller must release the interface.

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
<dt><b>MF_E_PROPERTY_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No metadata is available for the requested stream or presentation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider">IMFMetadataProvider</a>



<a href="/windows/desktop/medfound/media-metadata">Media Metadata</a>