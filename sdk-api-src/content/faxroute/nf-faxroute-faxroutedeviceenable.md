---
UID: NF:faxroute.FaxRouteDeviceEnable
title: FaxRouteDeviceEnable function
author: windows-driver-content
description: The FaxRouteDeviceEnable function allows a fax routing extension DLL to query, enable, or disable a fax routing method for a specific fax device. Each fax routing extension must export the FaxRouteDeviceEnable function.
old-location: fax\_mfax_faxroutedeviceenable.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_771h.htm
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: FaxRouteDeviceEnable, FaxRouteDeviceEnable function [Fax Service], QUERY_STATUS, STATUS_DISABLE, STATUS_ENABLE, _mfax_faxroutedeviceenable, fax._mfax_faxroutedeviceenable, faxroute/FaxRouteDeviceEnable
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
req.typenames: FAX_SEND, *PFAX_SEND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	FaxRoute.h
api_name:
-	FaxRouteDeviceEnable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
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

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, described in MSDN.

This function will return ERROR_BAD_CONFIGURATION if you attempt to refer to a device that is not configured, such as a folder that has not been specified, or a printer that does not exist on your network.




## -see-also




<a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/339f7fb6-64eb-403e-91be-210501042a25">Fax Routing Extension Functions</a>



<a href="https://msdn.microsoft.com/c9cf7b62-9a92-4b80-bd5b-6669817b3ad5">FaxRouteDeviceChangeNotification</a>
 

 

