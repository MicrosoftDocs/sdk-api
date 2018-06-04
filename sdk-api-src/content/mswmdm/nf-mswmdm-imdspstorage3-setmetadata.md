---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

