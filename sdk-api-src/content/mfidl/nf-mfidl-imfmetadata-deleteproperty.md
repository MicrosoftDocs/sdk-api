---
UID: NF:mfidl.IMFMetadata.DeleteProperty
title: IMFMetadata::DeleteProperty (mfidl.h)
description: Deletes a metadata property.
helpviewer_keywords: ["7c9a406d-6144-4e9c-b62c-1d9c691391f0","DeleteProperty","DeleteProperty method [Media Foundation]","DeleteProperty method [Media Foundation]","IMFMetadata interface","IMFMetadata interface [Media Foundation]","DeleteProperty method","IMFMetadata.DeleteProperty","IMFMetadata::DeleteProperty","mf.imfmetadata_deleteproperty","mfidl/IMFMetadata::DeleteProperty"]
old-location: mf\imfmetadata_deleteproperty.htm
tech.root: mf
ms.assetid: 7c9a406d-6144-4e9c-b62c-1d9c691391f0
ms.date: 12/05/2018
ms.keywords: 7c9a406d-6144-4e9c-b62c-1d9c691391f0, DeleteProperty, DeleteProperty method [Media Foundation], DeleteProperty method [Media Foundation],IMFMetadata interface, IMFMetadata interface [Media Foundation],DeleteProperty method, IMFMetadata.DeleteProperty, IMFMetadata::DeleteProperty, mf.imfmetadata_deleteproperty, mfidl/IMFMetadata::DeleteProperty
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
 - IMFMetadata::DeleteProperty
 - mfidl/IMFMetadata::DeleteProperty
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
 - IMFMetadata.DeleteProperty
---

# IMFMetadata::DeleteProperty


## -description

Deletes a metadata property.

## -parameters

### -param pwszName [in]

Pointer to a null-terminated string containing the name of the property.

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
The property was not found.
              

</td>
</tr>
</table>

## -remarks

For a media source, deleting a property from the metadata collection does not change the original content.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadata">IMFMetadata</a>



<a href="/windows/desktop/medfound/media-metadata">Media Metadata</a>