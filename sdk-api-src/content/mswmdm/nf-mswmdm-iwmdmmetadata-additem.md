---
UID: NF:mswmdm.IWMDMMetaData.AddItem
title: IWMDMMetaData::AddItem (mswmdm.h)
description: The AddItem method adds a metadata property to the interface.
helpviewer_keywords: ["AddItem","AddItem method [windows Media Device Manager]","AddItem method [windows Media Device Manager]","IWMDMMetaData interface","IWMDMMetaData interface [windows Media Device Manager]","AddItem method","IWMDMMetaData.AddItem","IWMDMMetaData::AddItem","IWMDMMetaDataAddItem","mswmdm/IWMDMMetaData::AddItem","wmdm.iwmdmmetadata_additem"]
old-location: wmdm\iwmdmmetadata_additem.htm
tech.root: WMDM
ms.assetid: fb8dee5f-034f-4e1d-86fe-34a2d9439e5f
ms.date: 12/05/2018
ms.keywords: AddItem, AddItem method [windows Media Device Manager], AddItem method [windows Media Device Manager],IWMDMMetaData interface, IWMDMMetaData interface [windows Media Device Manager],AddItem method, IWMDMMetaData.AddItem, IWMDMMetaData::AddItem, IWMDMMetaDataAddItem, mswmdm/IWMDMMetaData::AddItem, wmdm.iwmdmmetadata_additem
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMMetaData::AddItem
 - mswmdm/IWMDMMetaData::AddItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMMetaData.AddItem
---

# IWMDMMetaData::AddItem


## -description

The <b>AddItem</b> method adds a metadata property to the interface.

## -parameters

### -param Type [in]

An <a href="/windows/desktop/WMDM/wmdm-tag-datatype">WMDM_TAG_DATATYPE</a> enumerated value specifying the type of metadata being saved.

### -param pwszTagName [in]

Pointer to a wide-character, null-terminated string specifying the name of the property to set. A list of standard property name constants is given in <a href="/windows/desktop/WMDM/metadata-constants">Metadata Constants</a>.

### -param pValue [in]

Pointer to a byte array specifying the value to assign to the property. The submitted value is copied, so the memory can be freed after calling <b>AddItem</b>.

### -param iLength [in]

Integer specifying the size of <i>pValue</i>, in bytes.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata">IWMDMMetaData Interface</a>



<a href="/windows/desktop/WMDM/metadata-constants">Metadata Constants</a>



<a href="/windows/desktop/WMDM/setting-metadata-on-a-file">Setting Metadata on a File</a>