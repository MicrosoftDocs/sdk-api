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

# IMDSPDevice::GetSerialNumber


## -description



The <b>GetSerialNumber</b> method retrieves the serial number that uniquely identifies the device.




## -parameters




### -param pSerialNumber [out]

Pointer to a <b>WMDMID</b> structure that receives the serial number for the device. This parameter is included in the output message authentication code.


### -param abMac [in, out]

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



Not all media devices support serial numbers. To determine whether the device supports serial numbers, always check the return code when calling this method. If a media device does support serial numbers, the serial number of the media device is guaranteed to be unique.

This method is optional. When transferring protected content, Windows Media Device Manager uses <a href="https://msdn.microsoft.com/42765429-c230-4fa1-9e2e-e21c71e49ae0">IMDSPStorageGlobals::GetSerialNumber</a>. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice Interface</a>



<a href="https://msdn.microsoft.com/42765429-c230-4fa1-9e2e-e21c71e49ae0">IMDSPStorageGlobals::GetSerialNumber</a>
 

 

