---
UID: NF:mswmdm.IWMDMDevice.GetDeviceIcon
title: IWMDMDevice::GetDeviceIcon
author: windows-driver-content
description: The GetDeviceIcon method retrieves a handle to the icon that the device manufacturer wants to display when the device is connected.
old-location: wmdm\iwmdmdevice_getdeviceicon.htm
old-project: WMDM
ms.assetid: 55da3443-ad5b-469d-a493-0e2e8ea21f0c
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetDeviceIcon, GetDeviceIcon method [windows Media Device Manager], GetDeviceIcon method [windows Media Device Manager],IWMDMDevice interface, IWMDMDevice interface [windows Media Device Manager],GetDeviceIcon method, IWMDMDevice.GetDeviceIcon, IWMDMDevice::GetDeviceIcon, IWMDMDeviceGetDeviceIcon, mswmdm/IWMDMDevice::GetDeviceIcon, wmdm.iwmdmdevice_getdeviceicon
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
-	IWMDMDevice.GetDeviceIcon
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IWMDMDevice::GetDeviceIcon


## -description



The <b>GetDeviceIcon</b> method retrieves a handle to the icon that the device manufacturer wants to display when the device is connected.




## -parameters




### -param hIcon [out]

Handle to an icon object.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



When the application is finished with the icon, it must call the Win32 <b>DestroyIcon</b> function to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/44212da9-a38a-4ed5-86af-cf60b40bb54d">IWMDMDevice Interface</a>
 

 

