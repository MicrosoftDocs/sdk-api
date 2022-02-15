---
UID: NF:mfidl.IMFMetadata.GetProperty
title: IMFMetadata::GetProperty (mfidl.h)
description: Gets the value of a metadata property.
helpviewer_keywords: ["177c8612-5c9f-4a71-9ee1-a4c67737af2d","GetProperty","GetProperty method [Media Foundation]","GetProperty method [Media Foundation]","IMFMetadata interface","IMFMetadata interface [Media Foundation]","GetProperty method","IMFMetadata.GetProperty","IMFMetadata::GetProperty","mf.imfmetadata_getproperty","mfidl/IMFMetadata::GetProperty"]
old-location: mf\imfmetadata_getproperty.htm
tech.root: mf
ms.assetid: 177c8612-5c9f-4a71-9ee1-a4c67737af2d
ms.date: 12/05/2018
ms.keywords: 177c8612-5c9f-4a71-9ee1-a4c67737af2d, GetProperty, GetProperty method [Media Foundation], GetProperty method [Media Foundation],IMFMetadata interface, IMFMetadata interface [Media Foundation],GetProperty method, IMFMetadata.GetProperty, IMFMetadata::GetProperty, mf.imfmetadata_getproperty, mfidl/IMFMetadata::GetProperty
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
 - IMFMetadata::GetProperty
 - mfidl/IMFMetadata::GetProperty
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
 - IMFMetadata.GetProperty
---

# IMFMetadata::GetProperty


## -description

Gets the value of a metadata property.

## -parameters

### -param pwszName [in]

A pointer to a null-terminated string that contains the name of the property.
          To get the list of property names, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames">IMFMetadata::GetAllPropertyNames</a>.

### -param ppvValue [out]

Pointer to a <b>PROPVARIANT</b> that receives the value of the property. The <b>PROPVARIANT</b> type depends on the property. For multivalued properties, the <b>PROPVARIANT</b> is a <b>VT_VECTOR</b> type. The caller must free the <b>PROPVARIANT</b> by calling <a href="/windows/desktop/api/propidl/nf-propidl-propvariantclear">PropVariantClear</a>.

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
The requested property was not found.
              

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadata">IMFMetadata</a>



<a href="/windows/desktop/medfound/media-metadata">Media Metadata</a>