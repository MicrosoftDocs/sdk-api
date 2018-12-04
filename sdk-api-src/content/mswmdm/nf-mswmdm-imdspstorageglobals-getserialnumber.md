---
UID: NF:mswmdm.IMDSPStorageGlobals.GetSerialNumber
title: IMDSPStorageGlobals::GetSerialNumber
author: windows-sdk-content
description: The GetSerialNumber method retrieves a serial number uniquely identifying the storage medium. This method must be implemented for protected content transfer, but otherwise it is optional. For more information, see Mandatory and Optional Interfaces.
old-location: wmdm\imdspstorageglobals_getserialnumber.htm
tech.root: WMDM
ms.assetid: 42765429-c230-4fa1-9e2e-e21c71e49ae0
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetSerialNumber, GetSerialNumber method [windows Media Device Manager], GetSerialNumber method [windows Media Device Manager],IMDSPStorageGlobals interface, IMDSPStorageGlobals interface [windows Media Device Manager],GetSerialNumber method, IMDSPStorageGlobals.GetSerialNumber, IMDSPStorageGlobals::GetSerialNumber, IMDSPStorageGlobalsGetSerialNumber, mswmdm/IMDSPStorageGlobals::GetSerialNumber, wmdm.imdspstorageglobals_getserialnumber
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
 - IMDSPStorageGlobals.GetSerialNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPStorageGlobals::GetSerialNumber


## -description



The <b>GetSerialNumber</b> method retrieves a serial number uniquely identifying the storage medium. This method must be implemented for protected content transfer, but otherwise it is optional. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.



.


## -parameters




### -param pSerialNum [out]

Pointer to a <b>WMDMID</b> structure containing the serial number information. This parameter is included in the output message authentication code.


### -param abMac [in, out]

Array of eight bytes containing the message authentication code for the parameter data of this method. (WMDM_MAC_LENGTH is defined as 8.)


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



Not all storage media support serial numbers. The return code must always be checked to determine whether the storage medium provides this support. If the storage medium does not support returning a unique serial number, protected content cannot be transferred to the medium. If the storage represented is removable media, the serial number returned must be the storage serial number, which should be distinct from the device serial number.




## -see-also




<a href="https://msdn.microsoft.com/70653352-a467-4197-93e3-e8fb45f99d34">IMDSPStorageGlobals Interface</a>



<a href="https://msdn.microsoft.com/eaa5786e-a2a1-42d7-b527-be83d944cb20">WMDMID</a>
 

 

