---
UID: NF:faxroute.FaxRouteDeviceChangeNotification
title: FaxRouteDeviceChangeNotification function
author: windows-sdk-content
description: The fax service calls the FaxRouteDeviceChangeNotification function to inform a fax routing extension DLL that a fax device has been removed from the fax server, or that a new fax device has been installed.
old-location: fax\_mfax_faxroutedevicechangenotification.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_7gry.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: FaxRouteDeviceChangeNotification, FaxRouteDeviceChangeNotification function [Fax Service], _mfax_faxroutedevicechangenotification, fax._mfax_faxroutedevicechangenotification, faxroute/FaxRouteDeviceChangeNotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: faxroute.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - FaxRoute.h
api_name:
 - FaxRouteDeviceChangeNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxRouteDeviceChangeNotification function


## -description


The fax service calls the <b>FaxRouteDeviceChangeNotification</b> function to inform a fax routing extension DLL that a fax device has been removed from the fax server, or that a new fax device has been installed. Each fax routing extension must export the <b>FaxRouteDeviceChangeNotification</b> function.


## -parameters




### -param DeviceId [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that is the device identifier of the fax device that has been removed or installed. 


### -param NewDevice [in]

Type: <b>BOOL</b>

Specifies a Boolean variable that indicates whether the <i>DeviceId</i> parameter identifies a new device. If this parameter is equal to <b>TRUE</b>, the device is a new device. For more information, see the following Remarks section.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, described in MSDN.




## -remarks



If the <i>NewDevice</i> parameter is equal to <b>TRUE</b>, it indicates that the fax service detects the installation of a new fax device. The fax routing extension must perform any initialization procedures necessary to enable the extension to route inbound fax transmissions using the new device.

If the <i>NewDevice</i> parameter is equal to <b>FALSE</b>, it indicates that the fax service detects the removal of the fax device identified by the <i>DeviceId</i> parameter. The fax routing extension should perform required cleanup routines at this time.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684519(v=VS.85).aspx">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692865(v=VS.85).aspx">Fax Routing Extension Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692902(v=VS.85).aspx">FaxRouteDeviceEnable</a>
 

 

