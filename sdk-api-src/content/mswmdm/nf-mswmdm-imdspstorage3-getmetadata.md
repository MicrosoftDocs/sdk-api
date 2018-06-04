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
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



The service provider calls <a href="https://msdn.microsoft.com/fb8dee5f-034f-4e1d-86fe-34a2d9439e5f">IWMDMMetaData::AddItem</a> for each of the metadata properties to be sent to the application. The service provider should use the predefined metadata name tags (g_wszWMDMTitle, g_wszAlbumTitle, g_dwBitrate, and so on) contained in the mswmdm.h file.




## -see-also




<a href="https://msdn.microsoft.com/5ff674a1-a0b9-43b6-b8b7-9a5c67b3f919">IMDSPStorage3 Interface</a>



<a href="https://msdn.microsoft.com/bfb9a1e4-3cf6-4605-9613-d93f9cce201b">IMDSPStorage3::SetMetadata</a>



<a href="https://msdn.microsoft.com/ea57a851-0b9f-444c-9819-a278f2ece2b0">IWMDMMetaData Interface</a>
 

 

