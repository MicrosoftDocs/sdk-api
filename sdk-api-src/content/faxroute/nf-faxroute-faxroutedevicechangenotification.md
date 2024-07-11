---
UID: NF:faxroute.FaxRouteDeviceChangeNotification
title: FaxRouteDeviceChangeNotification function (faxroute.h)
description: The fax service calls the FaxRouteDeviceChangeNotification function to inform a fax routing extension DLL that a fax device has been removed from the fax server, or that a new fax device has been installed.
helpviewer_keywords: ["FaxRouteDeviceChangeNotification","FaxRouteDeviceChangeNotification function [Fax Service]","_mfax_faxroutedevicechangenotification","fax._mfax_faxroutedevicechangenotification","faxroute/FaxRouteDeviceChangeNotification"]
old-location: fax\_mfax_faxroutedevicechangenotification.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_7gry.htm
ms.date: 12/05/2018
ms.keywords: FaxRouteDeviceChangeNotification, FaxRouteDeviceChangeNotification function [Fax Service], _mfax_faxroutedevicechangenotification, fax._mfax_faxroutedevicechangenotification, faxroute/FaxRouteDeviceChangeNotification
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FaxRouteDeviceChangeNotification
 - faxroute/FaxRouteDeviceChangeNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - FaxRoute.h
api_name:
 - FaxRouteDeviceChangeNotification
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

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the <i>NewDevice</i> parameter is equal to <b>TRUE</b>, it indicates that the fax service detects the installation of a new fax device. The fax routing extension must perform any initialization procedures necessary to enable the extension to route inbound fax transmissions using the new device.

If the <i>NewDevice</i> parameter is equal to <b>FALSE</b>, it indicates that the fax service detects the removal of the fax device identified by the <i>DeviceId</i> parameter. The fax routing extension should perform required cleanup routines at this time.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-routing-extension-api">Fax Routing Extension Application Programming Interface Overview</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-routing-extension-functions">Fax Routing Extension Functions</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nf-faxroute-faxroutedeviceenable">FaxRouteDeviceEnable</a>