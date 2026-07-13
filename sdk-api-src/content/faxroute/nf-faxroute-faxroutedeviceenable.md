---
UID: NF:faxroute.FaxRouteDeviceEnable
title: FaxRouteDeviceEnable function (faxroute.h)
description: The FaxRouteDeviceEnable function allows a fax routing extension DLL to query, enable, or disable a fax routing method for a specific fax device. Each fax routing extension must export the FaxRouteDeviceEnable function.
helpviewer_keywords: ["FaxRouteDeviceEnable","FaxRouteDeviceEnable function [Fax Service]","QUERY_STATUS","STATUS_DISABLE","STATUS_ENABLE","_mfax_faxroutedeviceenable","fax._mfax_faxroutedeviceenable","faxroute/FaxRouteDeviceEnable"]
old-location: fax\_mfax_faxroutedeviceenable.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_771h.htm
ms.date: 12/05/2018
ms.keywords: FaxRouteDeviceEnable, FaxRouteDeviceEnable function [Fax Service], QUERY_STATUS, STATUS_DISABLE, STATUS_ENABLE, _mfax_faxroutedeviceenable, fax._mfax_faxroutedeviceenable, faxroute/FaxRouteDeviceEnable
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
 - FaxRouteDeviceEnable
 - faxroute/FaxRouteDeviceEnable
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
 - FaxRouteDeviceEnable
---

# FaxRouteDeviceEnable function


## -description

The <b>FaxRouteDeviceEnable</b> function allows a fax routing extension DLL to query, enable, or disable a fax routing method for a specific fax device. Each fax routing extension must export the <b>FaxRouteDeviceEnable</b> function.

## -parameters

### -param RoutingGuid [in]

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that contains the GUID for the fax routing method of interest.

### -param DeviceId [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that is the device identifier for the fax device of interest.

### -param Enabled [in]

Type: <b>LONG</b>

Specifies an enabled status for the fax routing method and fax device combination specified by the <i>RoutingGuid</i> and <i>DeviceId</i> parameters.
                    

The <i>Enabled</i> parameter can have one of the following values.



#### QUERY_STATUS

Return the current status of the specified routing method on the specified fax device. A value of <b>TRUE</b> indicates the routing method is enabled on the device; a value of <b>FALSE</b> indicates the routing method is disabled on the device.



#### STATUS_DISABLE

Disable the specified fax routing method on the specified fax device.



#### STATUS_ENABLE

Enable the specified fax routing method on the specified fax device.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

This function will return ERROR_BAD_CONFIGURATION if you attempt to refer to a device that is not configured, such as a folder that has not been specified, or a printer that does not exist on your network.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-routing-extension-api">Fax Routing Extension Application Programming Interface Overview</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-routing-extension-functions">Fax Routing Extension Functions</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nf-faxroute-faxroutedevicechangenotification">FaxRouteDeviceChangeNotification</a>