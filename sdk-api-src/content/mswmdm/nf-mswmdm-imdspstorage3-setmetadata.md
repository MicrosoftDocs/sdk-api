---
UID: NF:mswmdm.IMDSPStorage3.SetMetadata
title: IMDSPStorage3::SetMetadata
author: windows-sdk-content
description: The SetMetadata method provides the metadata associated with a specified content.
old-location: wmdm\imdspstorage3_setmetadata.htm
old-project: WMDM
ms.assetid: bfb9a1e4-3cf6-4605-9613-d93f9cce201b
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IMDSPStorage3 interface [windows Media Device Manager],SetMetadata method, IMDSPStorage3.SetMetadata, IMDSPStorage3::SetMetadata, IMDSPStorage3SetMetadata, SetMetadata, SetMetadata method [windows Media Device Manager], SetMetadata method [windows Media Device Manager],IMDSPStorage3 interface, mswmdm/IMDSPStorage3::SetMetadata, wmdm.imdspstorage3_setmetadata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MSVidCtlStateList
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
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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




<a href="https://msdn.microsoft.com/5ff674a1-a0b9-43b6-b8b7-9a5c67b3f919">IMDSPStorage3 Interface</a>



<a href="https://msdn.microsoft.com/a341289b-79e6-4ac7-b0d3-72ad5953c1df">IMDSPStorage3::GetMetadata</a>



<a href="https://msdn.microsoft.com/ea57a851-0b9f-444c-9819-a278f2ece2b0">IWMDMMetaData Interface</a>



<a href="https://msdn.microsoft.com/5d27e1e9-ab91-433d-8216-ace195386d44">IWMDMMetaData::QueryByIndex</a>



<a href="https://msdn.microsoft.com/e793954b-6aef-4088-97cb-eb1f050cc64b">IWMDMMetaData::QueryByName</a>
 

 

