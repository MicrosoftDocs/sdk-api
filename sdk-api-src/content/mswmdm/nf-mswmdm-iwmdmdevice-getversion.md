---
UID: NF:mswmdm.IWMDMDevice.GetVersion
title: IWMDMDevice::GetVersion
author: windows-sdk-content
description: The GetVersion method retrieves the manufacturer-defined version number of the device.
old-location: wmdm\iwmdmdevice_getversion.htm
tech.root: WMDM
ms.assetid: ae0253f2-30cd-46d0-b9e9-f2cb878c1ff3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetVersion, GetVersion method [windows Media Device Manager], GetVersion method [windows Media Device Manager],IWMDMDevice interface, IWMDMDevice interface [windows Media Device Manager],GetVersion method, IWMDMDevice.GetVersion, IWMDMDevice::GetVersion, IWMDMDeviceGetVersion, mswmdm/IWMDMDevice::GetVersion, wmdm.iwmdmdevice_getversion
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
 - IWMDMDevice.GetVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMDevice::GetVersion


## -description



The <b>GetVersion</b> method retrieves the manufacturer-defined version number of the device.




## -parameters




### -param pdwVersion [out]

Pointer to a <b>DWORD</b> specifying the version number.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



The format of the version number is determined by the manufacturer.




## -see-also




<a href="https://msdn.microsoft.com/44212da9-a38a-4ed5-86af-cf60b40bb54d">IWMDMDevice Interface</a>
 

 

