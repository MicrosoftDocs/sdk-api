---
UID: NF:mswmdm.IMDSPStorage.GetSize
title: IMDSPStorage::GetSize method
author: windows-driver-content
description: The GetSize method retrieves the size of the storage object, in bytes.
old-location: wmdm\imdspstorage_getsize.htm
old-project: WMDM
ms.assetid: 95b28f9a-744c-4d49-a91c-6652d688b91a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetSize method [windows Media Device Manager], GetSize method [windows Media Device Manager], IMDSPStorage interface, GetSize,IMDSPStorage.GetSize, IMDSPStorage, IMDSPStorage interface [windows Media Device Manager], GetSize method, IMDSPStorage::GetSize, IMDSPStorageGetSize, mswmdm/IMDSPStorage::GetSize, wmdm.imdspstorage_getsize
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IMDSPStorage.GetSize
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMDSPStorage::GetSize method


## -description



The <b>GetSize</b> method retrieves the size of the storage object, in bytes.




## -parameters




### -param pdwSizeLow [out]

Pointer to a <b>DWORD</b> containing the low-order part of the storage object size.


### -param pdwSizeHigh [out]

Pointer to a <b>DWORD</b> containing the high-order part of the storage object size.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



The object size is reported in bytes. The size is zero for folder objects.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage Interface</a>



<a href="https://msdn.microsoft.com/4ba0c598-9ea2-42cc-a234-1c0e192971a8">IMDSPStorage::GetDate</a>



<a href="https://msdn.microsoft.com/6172f222-8b92-4da5-8001-b79431c26518">IMDSPStorage::GetName</a>
 

 

