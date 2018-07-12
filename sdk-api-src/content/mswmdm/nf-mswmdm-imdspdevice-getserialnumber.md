---
UID: NF:mswmdm.IMDSPDevice.GetSerialNumber
title: IMDSPDevice::GetSerialNumber
author: windows-sdk-content
description: The GetSerialNumber method retrieves the serial number that uniquely identifies the device.
old-location: wmdm\imdspdevice_getserialnumber.htm
old-project: WMDM
ms.assetid: dfff9660-fc74-421c-91d2-3d6be1c753da
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetSerialNumber, GetSerialNumber method [windows Media Device Manager], GetSerialNumber method [windows Media Device Manager],IMDSPDevice interface, IMDSPDevice interface [windows Media Device Manager],GetSerialNumber method, IMDSPDevice.GetSerialNumber, IMDSPDevice::GetSerialNumber, IMDSPDeviceGetSerialNumber, mswmdm/IMDSPDevice::GetSerialNumber, wmdm.imdspdevice_getserialnumber
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
 - IMDSPDevice.GetSerialNumber
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

