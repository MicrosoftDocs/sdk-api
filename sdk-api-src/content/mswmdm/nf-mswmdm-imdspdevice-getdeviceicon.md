---
UID: NF:mswmdm.IMDSPDevice.GetDeviceIcon
title: IMDSPDevice::GetDeviceIcon
author: windows-driver-content
description: The GetDeviceIcon method returns a HICON that represents the icon that the device service provider indicates must be used to represent this device.
old-location: wmdm\imdspdevice_getdeviceicon.htm
old-project: WMDM
ms.assetid: 0a7fcae6-cf7f-4b78-847c-de9db8c32871
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: GetDeviceIcon, GetDeviceIcon method [windows Media Device Manager], GetDeviceIcon method [windows Media Device Manager],IMDSPDevice interface, IMDSPDevice interface [windows Media Device Manager],GetDeviceIcon method, IMDSPDevice.GetDeviceIcon, IMDSPDevice::GetDeviceIcon, IMDSPDeviceGetDeviceIcon, mswmdm/IMDSPDevice::GetDeviceIcon, wmdm.imdspdevice_getdeviceicon
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
-	IMDSPDevice.GetDeviceIcon
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMDSPDevice::GetDeviceIcon


## -description



The <b>GetDeviceIcon</b> method returns a <b>HICON</b> that represents the icon that the device service provider indicates must be used to represent this device.




## -parameters




### -param hIcon [out]

Handle to an <b>Icon</b> object that receives the icon for the device. Before using it, the caller must cast the value to a <b>HICON</b>*. When an application is finished with the icon, it should call <b>DestroyIcon</b> to free the resource. <b>DestroyIcon</b> is a standard Win32 function.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



In addition to the values above, the <b>HRESULT</b> error code could be a Win32 error.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice Interface</a>
 

 

