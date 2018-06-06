---
UID: NF:mswmdm.IMDSPStorage3.GetMetadata
title: IMDSPStorage3::GetMetadata
author: windows-sdk-content
description: The GetMetadata method retrieves metadata from the service provider.
old-location: wmdm\imdspstorage3_getmetadata.htm
old-project: WMDM
ms.assetid: a341289b-79e6-4ac7-b0d3-72ad5953c1df
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetMetadata, GetMetadata method [windows Media Device Manager], GetMetadata method [windows Media Device Manager],IMDSPStorage3 interface, IMDSPStorage3 interface [windows Media Device Manager],GetMetadata method, IMDSPStorage3.GetMetadata, IMDSPStorage3::GetMetadata, IMDSPStorage3GetMetadata, mswmdm/IMDSPStorage3::GetMetadata, wmdm.imdspstorage3_getmetadata
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
 - IMDSPStorage3.GetMetadata
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

