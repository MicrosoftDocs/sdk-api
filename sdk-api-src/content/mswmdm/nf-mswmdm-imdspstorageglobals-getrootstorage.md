---
UID: NF:mswmdm.IMDSPStorageGlobals.GetRootStorage
title: IMDSPStorageGlobals::GetRootStorage
author: windows-sdk-content
description: The GetRootStorage method retrieves a pointer to the IMDSPStorage interface for the root storage of the storage medium.
old-location: wmdm\imdspstorageglobals_getrootstorage.htm
old-project: WMDM
ms.assetid: 80b6cb71-d567-4fb5-9f75-82ae2fe118c7
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetRootStorage, GetRootStorage method [windows Media Device Manager], GetRootStorage method [windows Media Device Manager],IMDSPStorageGlobals interface, IMDSPStorageGlobals interface [windows Media Device Manager],GetRootStorage method, IMDSPStorageGlobals.GetRootStorage, IMDSPStorageGlobals::GetRootStorage, IMDSPStorageGlobalsGetRootStorage, mswmdm/IMDSPStorageGlobals::GetRootStorage, wmdm.imdspstorageglobals_getrootstorage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.redist: 
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
 - IMDSPStorageGlobals.GetRootStorage
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPStorageGlobals::GetRootStorage


## -description



The <b>GetRootStorage</b> method retrieves a pointer to the <b>IMDSPStorage</b> interface for the root storage of the storage medium.




## -parameters




### -param ppRoot [out]

Pointer to an <b>IMDSPStorage</b> pointer that receives the root storage.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage Interface</a>



<a href="https://msdn.microsoft.com/70653352-a467-4197-93e3-e8fb45f99d34">IMDSPStorageGlobals Interface</a>



<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>
 

 

