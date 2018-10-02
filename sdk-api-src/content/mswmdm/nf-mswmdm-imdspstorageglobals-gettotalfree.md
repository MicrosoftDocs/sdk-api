---
UID: NF:mswmdm.IMDSPStorageGlobals.GetTotalFree
title: IMDSPStorageGlobals::GetTotalFree
author: windows-sdk-content
description: The GetTotalFree method retrieves the total free space on the storage medium, in bytes.
old-location: wmdm\imdspstorageglobals_gettotalfree.htm
tech.root: WMDM
ms.assetid: 141b33e8-5cb5-46a8-b91e-01bd9c634cbf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetTotalFree, GetTotalFree method [windows Media Device Manager], GetTotalFree method [windows Media Device Manager],IMDSPStorageGlobals interface, IMDSPStorageGlobals interface [windows Media Device Manager],GetTotalFree method, IMDSPStorageGlobals.GetTotalFree, IMDSPStorageGlobals::GetTotalFree, IMDSPStorageGlobalsGetTotalFree, mswmdm/IMDSPStorageGlobals::GetTotalFree, wmdm.imdspstorageglobals_gettotalfree
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPStorageGlobals.GetTotalFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPStorageGlobals::GetTotalFree


## -description



The <b>GetTotalFree</b> method retrieves the total free space on the storage medium, in bytes.




## -parameters




### -param pdwFreeLow [out]

Pointer to a <b>DWORD</b> containing the low-order bytes of the free space.


### -param pdwFreeHigh [out]

Pointer to a <b>DWORD</b> containing the high-order bytes of the free space.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



To determine the amount of storage space in use by the medium for file management, subtract the number of bad bytes identified by using <b>GetTotalBad</b> from the number of free bytes identified by using <b>GetTotalFree</b>.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/70653352-a467-4197-93e3-e8fb45f99d34">IMDSPStorageGlobals Interface</a>



<a href="https://msdn.microsoft.com/6a4b4ac5-0b7e-4a22-9857-b251a6bf1dcf">IMDSPStorageGlobals::GetTotalSize</a>
 

 

