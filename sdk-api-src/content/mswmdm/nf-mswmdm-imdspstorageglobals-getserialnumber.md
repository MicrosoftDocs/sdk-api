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

# IMDSPStorageGlobals::GetSerialNumber


## -description



The <b>GetSerialNumber</b> method retrieves a serial number uniquely identifying the storage medium. This method must be implemented for protected content transfer, but otherwise it is optional. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.



.


## -parameters




### -param pSerialNum [out]

Pointer to a <b>WMDMID</b> structure containing the serial number information. This parameter is included in the output message authentication code.


### -param abMac






#### - abMac[WMDM_MAC_LENGTH] [in, out]

Array of eight bytes containing the message authentication code for the parameter data of this method. (WMDM_MAC_LENGTH is defined as 8.)


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



Not all storage media support serial numbers. The return code must always be checked to determine whether the storage medium provides this support. If the storage medium does not support returning a unique serial number, protected content cannot be transferred to the medium. If the storage represented is removable media, the serial number returned must be the storage serial number, which should be distinct from the device serial number.




## -see-also




<a href="https://msdn.microsoft.com/70653352-a467-4197-93e3-e8fb45f99d34">IMDSPStorageGlobals Interface</a>



<a href="https://msdn.microsoft.com/eaa5786e-a2a1-42d7-b527-be83d944cb20">WMDMID</a>
 

 

