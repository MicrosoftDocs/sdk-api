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

# IWMDMStorageGlobals::GetTotalFree


## -description



The <b>GetTotalFree</b> method retrieves the total amount of free space on the storage medium, in bytes.




## -parameters




### -param pdwFreeLow [out]

Pointer to a <b>DWORD</b> that receives the low-order part of the free space value.


### -param pdwFreeHigh [out]

Pointer to a <b>DWORD</b> that receives the high-order part of the free space value.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



To determine the amount of storage space in use by the medium for file management, subtract the number of bad bytes retrieved using <a href="https://msdn.microsoft.com/40e1a39b-2757-472c-b585-77b829605e8c">GetTotalBad</a> from the number of free bytes retrieved using <b>GetTotalFree</b>.




## -see-also




<a href="https://msdn.microsoft.com/fe164271-58f0-4b28-a200-6b15f8b42d36">IWMDMStorageGlobals Interface</a>



<a href="https://msdn.microsoft.com/40e1a39b-2757-472c-b585-77b829605e8c">IWMDMStorageGlobals::GetTotalBad</a>



<a href="https://msdn.microsoft.com/ebbc8b7e-037f-4b8d-b026-793d38914685">IWMDMStorageGlobals::GetTotalSize</a>
 

 

