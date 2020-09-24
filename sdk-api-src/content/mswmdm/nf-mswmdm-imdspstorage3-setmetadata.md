---
UID: NF:mswmdm.IMDSPStorage3.SetMetadata
title: IMDSPStorage3::SetMetadata (mswmdm.h)
description: The SetMetadata method provides the metadata associated with a specified content.
helpviewer_keywords: ["IMDSPStorage3 interface [windows Media Device Manager]","SetMetadata method","IMDSPStorage3.SetMetadata","IMDSPStorage3::SetMetadata","IMDSPStorage3SetMetadata","SetMetadata","SetMetadata method [windows Media Device Manager]","SetMetadata method [windows Media Device Manager]","IMDSPStorage3 interface","mswmdm/IMDSPStorage3::SetMetadata","wmdm.imdspstorage3_setmetadata"]
old-location: wmdm\imdspstorage3_setmetadata.htm
tech.root: WMDM
ms.assetid: bfb9a1e4-3cf6-4605-9613-d93f9cce201b
ms.date: 12/05/2018
ms.keywords: IMDSPStorage3 interface [windows Media Device Manager],SetMetadata method, IMDSPStorage3.SetMetadata, IMDSPStorage3::SetMetadata, IMDSPStorage3SetMetadata, SetMetadata, SetMetadata method [windows Media Device Manager], SetMetadata method [windows Media Device Manager],IMDSPStorage3 interface, mswmdm/IMDSPStorage3::SetMetadata, wmdm.imdspstorage3_setmetadata
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
 - IMDSPStorage3::SetMetadata
 - mswmdm/IMDSPStorage3::SetMetadata
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
 - IMDSPStorage3.SetMetadata
---

# IMDSPStorage3::SetMetadata


## -description

The <b>SetMetadata</b> method provides the metadata associated with a specified content.

## -parameters

### -param pMetadata [in]

Pointer to an <b>IWMDMMetadata</b> interface.

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
The method succeeded, which indicates that SP has successfully processed the metadata.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The device does not support setting metadata.

</td>
</tr>
</table>

## -remarks

A service provider calls <b>IWMDMMetaData::QueryByName</b> or <b>IWMDMMetaData::QueryByIndex</b> to retrieve the metadata.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage3">IMDSPStorage3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage3-getmetadata">IMDSPStorage3::GetMetadata</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata">IWMDMMetaData Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-querybyindex">IWMDMMetaData::QueryByIndex</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-querybyname">IWMDMMetaData::QueryByName</a>