---
UID: NF:mswmdm.IWMDMMetaData.QueryByIndex
title: IWMDMMetaData::QueryByIndex (mswmdm.h)
description: The QueryByIndex method retrieves the value of a property specified by index.
helpviewer_keywords: ["IWMDMMetaData interface [windows Media Device Manager]","QueryByIndex method","IWMDMMetaData.QueryByIndex","IWMDMMetaData::QueryByIndex","IWMDMMetaDataQueryByIndex","QueryByIndex","QueryByIndex method [windows Media Device Manager]","QueryByIndex method [windows Media Device Manager]","IWMDMMetaData interface","mswmdm/IWMDMMetaData::QueryByIndex","wmdm.iwmdmmetadata_querybyindex"]
old-location: wmdm\iwmdmmetadata_querybyindex.htm
tech.root: WMDM
ms.assetid: 5d27e1e9-ab91-433d-8216-ace195386d44
ms.date: 12/05/2018
ms.keywords: IWMDMMetaData interface [windows Media Device Manager],QueryByIndex method, IWMDMMetaData.QueryByIndex, IWMDMMetaData::QueryByIndex, IWMDMMetaDataQueryByIndex, QueryByIndex, QueryByIndex method [windows Media Device Manager], QueryByIndex method [windows Media Device Manager],IWMDMMetaData interface, mswmdm/IWMDMMetaData::QueryByIndex, wmdm.iwmdmmetadata_querybyindex
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
 - IWMDMMetaData::QueryByIndex
 - mswmdm/IWMDMMetaData::QueryByIndex
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
 - IWMDMMetaData.QueryByIndex
---

# IWMDMMetaData::QueryByIndex


## -description

The <b>QueryByIndex</b> method retrieves the value of a property specified by index.

## -parameters

### -param iIndex [in]

Integer specifying the zero-based index of the property. The number of items is obtained through the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-getitemcount">GetItemCount</a> call.

### -param ppwszName [out]

Name of the property. Windows Media Device Manager allocates this memory, and the caller must free it using <b>CoTaskMemFree</b>.

### -param pType [out]

An <a href="/windows/desktop/WMDM/wmdm-tag-datatype">WMDM_TAG_DATATYPE</a> enumerated value describing the type of data returned in <i>ppValue</i>.

### -param ppValue [out]

Pointer to a pointer to a byte array that receives the content of the value if the method succeeds. This memory is allocated by Windows Media Device Manager, and the caller must free it using <b>CoTaskMemFree</b>.

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

<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-getitemcount">GetItemCount</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata">IWMDMMetaData Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-querybyname">QueryByName</a>



<a href="/windows/desktop/WMDM/setting-metadata-on-a-file">Setting Metadata on a File</a>