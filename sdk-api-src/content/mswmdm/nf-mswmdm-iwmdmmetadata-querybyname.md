---
UID: NF:mswmdm.IWMDMMetaData.QueryByName
title: IWMDMMetaData::QueryByName (mswmdm.h)
description: The QueryByName method retrieves the value of a property specified by name.
helpviewer_keywords: ["IWMDMMetaData interface [windows Media Device Manager]","QueryByName method","IWMDMMetaData.QueryByName","IWMDMMetaData::QueryByName","IWMDMMetaDataQueryByName","QueryByName","QueryByName method [windows Media Device Manager]","QueryByName method [windows Media Device Manager]","IWMDMMetaData interface","mswmdm/IWMDMMetaData::QueryByName","wmdm.iwmdmmetadata_querybyname"]
old-location: wmdm\iwmdmmetadata_querybyname.htm
tech.root: WMDM
ms.assetid: e793954b-6aef-4088-97cb-eb1f050cc64b
ms.date: 12/05/2018
ms.keywords: IWMDMMetaData interface [windows Media Device Manager],QueryByName method, IWMDMMetaData.QueryByName, IWMDMMetaData::QueryByName, IWMDMMetaDataQueryByName, QueryByName, QueryByName method [windows Media Device Manager], QueryByName method [windows Media Device Manager],IWMDMMetaData interface, mswmdm/IWMDMMetaData::QueryByName, wmdm.iwmdmmetadata_querybyname
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
 - IWMDMMetaData::QueryByName
 - mswmdm/IWMDMMetaData::QueryByName
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
 - IWMDMMetaData.QueryByName
---

# IWMDMMetaData::QueryByName


## -description

The <b>QueryByName</b> method retrieves the value of a property specified by name.

## -parameters

### -param pwszTagName [in]

Pointer to a wide-character <b>null</b>-terminated string specifying the property name. A list of standard property name constants is given in <a href="/windows/desktop/WMDM/metadata-constants">Metadata Constants</a>.

### -param pType [out]

An <a href="/windows/desktop/WMDM/wmdm-tag-datatype">WMDM_TAG_DATATYPE</a> enumerated value describing the type of data retrieved by <i>pValue</i>.

### -param pValue [out]

Pointer to a pointer to a byte array that receives the content of the value if the method succeeds. Windows Media Device Manager allocates this memory and the caller must free it using <b>CoTaskMemFree</b>.

### -param pcbLength [out]

Pointer to the size, in bytes, of the byte array <i>ppValue</i>. If the value is a string, this includes the termination character.

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



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-querybyindex">QueryByIndex</a>



<a href="/windows/desktop/WMDM/setting-metadata-on-a-file">Setting Metadata on a File</a>