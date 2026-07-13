---
UID: NF:faxroute.FaxRouteSetRoutingInfo
title: FaxRouteSetRoutingInfo function (faxroute.h)
description: The FaxRouteSetRoutingInfo function modifies routing configuration data for a specific fax device. Each fax routing extension DLL must export the FaxRouteSetRoutingInfo function.
helpviewer_keywords: ["FaxRouteSetRoutingInfo","FaxRouteSetRoutingInfo function [Fax Service]","_mfax_faxroutesetroutinginfo","fax._mfax_faxroutesetroutinginfo","faxroute/FaxRouteSetRoutingInfo"]
old-location: fax\_mfax_faxroutesetroutinginfo.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_89nz.htm
ms.date: 12/05/2018
ms.keywords: FaxRouteSetRoutingInfo, FaxRouteSetRoutingInfo function [Fax Service], _mfax_faxroutesetroutinginfo, fax._mfax_faxroutesetroutinginfo, faxroute/FaxRouteSetRoutingInfo
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
 - FaxRouteSetRoutingInfo
 - faxroute/FaxRouteSetRoutingInfo
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
 - FaxRouteSetRoutingInfo
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

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The fax service calls the <b>FaxRouteSetRoutingInfo</b> function to modify routing configuration data for a specific fax device.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-routing-extension-api">Fax Routing Extension Application Programming Interface Overview</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-routing-extension-functions">Fax Routing Extension Functions</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nf-faxroute-faxroutegetroutinginfo">FaxRouteGetRoutingInfo</a>