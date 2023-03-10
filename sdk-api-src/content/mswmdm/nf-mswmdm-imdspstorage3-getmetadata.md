---
UID: NF:mswmdm.IMDSPStorage3.GetMetadata
title: IMDSPStorage3::GetMetadata (mswmdm.h)
description: The GetMetadata method retrieves metadata from the service provider.
helpviewer_keywords: ["GetMetadata","GetMetadata method [windows Media Device Manager]","GetMetadata method [windows Media Device Manager]","IMDSPStorage3 interface","IMDSPStorage3 interface [windows Media Device Manager]","GetMetadata method","IMDSPStorage3.GetMetadata","IMDSPStorage3::GetMetadata","IMDSPStorage3GetMetadata","mswmdm/IMDSPStorage3::GetMetadata","wmdm.imdspstorage3_getmetadata"]
old-location: wmdm\imdspstorage3_getmetadata.htm
tech.root: WMDM
ms.assetid: a341289b-79e6-4ac7-b0d3-72ad5953c1df
ms.date: 12/05/2018
ms.keywords: GetMetadata, GetMetadata method [windows Media Device Manager], GetMetadata method [windows Media Device Manager],IMDSPStorage3 interface, IMDSPStorage3 interface [windows Media Device Manager],GetMetadata method, IMDSPStorage3.GetMetadata, IMDSPStorage3::GetMetadata, IMDSPStorage3GetMetadata, mswmdm/IMDSPStorage3::GetMetadata, wmdm.imdspstorage3_getmetadata
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
 - IMDSPStorage3::GetMetadata
 - mswmdm/IMDSPStorage3::GetMetadata
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
 - IMDSPStorage3.GetMetadata
---

# IMDSPStorage3::GetMetadata


## -description

The <b>GetMetadata</b> method retrieves metadata from the service provider.

## -parameters

### -param pMetadata [in]

Pointer to an <b>IWMDMMetaData</b> interface.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The service provider calls <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem">IWMDMMetaData::AddItem</a> for each of the metadata properties to be sent to the application. The service provider should use the predefined metadata name tags (g_wszWMDMTitle, g_wszAlbumTitle, g_dwBitrate, and so on) contained in the mswmdm.h file.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage3">IMDSPStorage3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage3-setmetadata">IMDSPStorage3::SetMetadata</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata">IWMDMMetaData Interface</a>