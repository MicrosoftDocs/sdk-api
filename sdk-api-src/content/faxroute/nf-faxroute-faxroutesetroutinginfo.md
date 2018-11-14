---
UID: NF:faxroute.FaxRouteSetRoutingInfo
title: FaxRouteSetRoutingInfo function
author: windows-sdk-content
description: The FaxRouteSetRoutingInfo function modifies routing configuration data for a specific fax device. Each fax routing extension DLL must export the FaxRouteSetRoutingInfo function.
old-location: fax\_mfax_faxroutesetroutinginfo.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_89nz.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: FaxRouteSetRoutingInfo, FaxRouteSetRoutingInfo function [Fax Service], _mfax_faxroutesetroutinginfo, fax._mfax_faxroutesetroutinginfo, faxroute/FaxRouteSetRoutingInfo
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
 - FaxRouteSetRoutingInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- FaxRouteSetRoutingInfo
: 
---

# FaxRouteSetRoutingInfo function


## -description


The <b>FaxRouteSetRoutingInfo</b> function modifies routing configuration data for a specific fax device. Each fax routing extension DLL must export the <b>FaxRouteSetRoutingInfo</b> function.


## -parameters




### -param RoutingGuid [in]

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that contains the GUID for the fax routing method.


### -param DeviceId [in]

Type: <b>DWORD</b>

Specifies the device identifier of the fax device that will have its routing configuration data modified. 


### -param RoutingInfo [in]

Type: <b>const BYTE*</b>

Pointer to a buffer that provides the fax routing configuration data.


### -param RoutingInfoSize [in]

Type: <b>DWORD</b>

Specifies the size, in bytes, of the buffer pointed to by the <i>RoutingInfo</i> parameter.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, described in MSDN.




## -remarks



The fax service calls the <b>FaxRouteSetRoutingInfo</b> function to modify routing configuration data for a specific fax device.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684519(v=VS.85).aspx">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692865(v=VS.85).aspx">Fax Routing Extension Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692861(v=VS.85).aspx">FaxRouteGetRoutingInfo</a>
 

 

