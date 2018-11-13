---
UID: NF:faxroute.FaxRouteGetRoutingInfo
title: FaxRouteGetRoutingInfo function
author: windows-sdk-content
description: The FaxRouteGetRoutingInfo function queries the fax routing extension DLL to obtain routing configuration data for a specific fax device. Each fax routing extension DLL must export the FaxRouteGetRoutingInfo function.
old-location: fax\_mfax_faxroutegetroutinginfo.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_3t2n.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: FaxRouteGetRoutingInfo, FaxRouteGetRoutingInfo function [Fax Service], _mfax_faxroutegetroutinginfo, fax._mfax_faxroutegetroutinginfo, faxroute/FaxRouteGetRoutingInfo
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
 - FaxRouteGetRoutingInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxRouteGetRoutingInfo function


## -description


The <b>FaxRouteGetRoutingInfo</b> function queries the fax routing extension DLL to obtain routing configuration data for a specific fax device. Each fax routing extension DLL must export the <b>FaxRouteGetRoutingInfo</b> function.


## -parameters




### -param RoutingGuid [in]

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that contains the GUID for the fax routing method.


### -param DeviceId [in]

Type: <b>DWORD</b>

Specifies the identifier of the fax device to query.


### -param RoutingInfo [in]

Type: <b>LPBYTE</b>

Pointer to a buffer that receives the fax routing configuration data.


### -param RoutingInfoSize [out]

Type: <b>LPDWORD</b>

Pointer to an unsigned <b>DWORD</b> variable that specifies the size, in bytes, of the buffer pointed to by the <i>RoutingInfo</i> parameter. For more information, see the following Remarks section.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, described in MSDN.




## -remarks



The fax service calls the <b>FaxRouteGetRoutingInfo</b> function twice. On the first call to the function the fax service passes a null pointer in the <i>RoutingInfo</i> parameter. The fax routing extension DLL must set the <i>RoutingInfoSize</i> parameter to the size required for the <i>RoutingInfo</i> buffer. The fax service calls <b>FaxRouteGetRoutingInfo</b> a second time with a valid pointer to the <i>RoutingInfo</i> buffer.




## -see-also




<a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/339f7fb6-64eb-403e-91be-210501042a25">Fax Routing Extension Functions</a>



<a href="https://msdn.microsoft.com/7c18c63d-e30e-4308-9b3a-d1ec4546a0f3">FaxRouteSetRoutingInfo</a>
 

 

