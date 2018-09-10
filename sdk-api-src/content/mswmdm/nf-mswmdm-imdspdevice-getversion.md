---
UID: NF:mswmdm.IMDSPDevice.GetVersion
title: IMDSPDevice::GetVersion
author: windows-sdk-content
description: The GetVersion method retrieves the version number of the device.
old-location: wmdm\imdspdevice_getversion.htm
tech.root: WMDM
ms.assetid: 88c935ad-dbf0-41bb-8676-ddafe9d1fe0e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetVersion, GetVersion method [windows Media Device Manager], GetVersion method [windows Media Device Manager],IMDSPDevice interface, IMDSPDevice interface [windows Media Device Manager],GetVersion method, IMDSPDevice.GetVersion, IMDSPDevice::GetVersion, IMDSPDeviceGetVersion, mswmdm/IMDSPDevice::GetVersion, wmdm.imdspdevice_getversion
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
 - IMDSPDevice.GetVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPDevice::GetVersion


## -description



The <b>GetVersion</b> method retrieves the version number of the device.




## -parameters




### -param pdwVersion [out]

Pointer to a <b>DWORD</b> to receive the version number of the device.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



This method is optional. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice Interface</a>
 

 

