---
UID: NN:mswmdm.IWMDMMetaData
title: IWMDMMetaData (mswmdm.h)
description: The IWMDMMetaData interface sets and retrieves metadata properties (such as artist, album, genre, and so on) of a storage.
helpviewer_keywords: ["IWMDMMetaData","IWMDMMetaData interface [windows Media Device Manager]","IWMDMMetaData interface [windows Media Device Manager]","described","IWMDMMetaDataInterface","mswmdm/IWMDMMetaData","wmdm.iwmdmmetadata"]
old-location: wmdm\iwmdmmetadata.htm
tech.root: WMDM
ms.assetid: ea57a851-0b9f-444c-9819-a278f2ece2b0
ms.date: 12/05/2018
ms.keywords: IWMDMMetaData, IWMDMMetaData interface [windows Media Device Manager], IWMDMMetaData interface [windows Media Device Manager],described, IWMDMMetaDataInterface, mswmdm/IWMDMMetaData, wmdm.iwmdmmetadata
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMMetaData
 - mswmdm/IWMDMMetaData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IWMDMMetaData
---

# IWMDMMetaData interface


## -description

The <b>IWMDMMetaData</b> interface sets and retrieves metadata properties (such as artist, album, genre, and so on) of a storage. Metadata properties are stored as name-value pairs.

To create a new, empty instance of this interface, call <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject">IWMDMStorage3::CreateEmptyMetadataObject</a>. To retrieve this interface (with values), call <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata">IWMDMStorage3::GetMetadata</a> or <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata">IWMDMStorage4::GetSpecifiedMetadata</a>.

## -inheritance

The <b>IWMDMMetaData</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMMetaData</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>



<a href="/windows/desktop/WMDM/metadata-constants">Metadata Constants</a>



<a href="/windows/desktop/WMDM/setting-metadata-on-a-file">Setting Metadata on a File</a>
