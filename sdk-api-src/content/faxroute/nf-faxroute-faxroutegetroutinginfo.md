---
UID: NF:faxroute.FaxRouteGetRoutingInfo
title: FaxRouteGetRoutingInfo function (faxroute.h)
description: The FaxRouteGetRoutingInfo function queries the fax routing extension DLL to obtain routing configuration data for a specific fax device. Each fax routing extension DLL must export the FaxRouteGetRoutingInfo function.
helpviewer_keywords: ["FaxRouteGetRoutingInfo","FaxRouteGetRoutingInfo function [Fax Service]","_mfax_faxroutegetroutinginfo","fax._mfax_faxroutegetroutinginfo","faxroute/FaxRouteGetRoutingInfo"]
old-location: fax\_mfax_faxroutegetroutinginfo.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_3t2n.htm
ms.date: 12/05/2018
ms.keywords: FaxRouteGetRoutingInfo, FaxRouteGetRoutingInfo function [Fax Service], _mfax_faxroutegetroutinginfo, fax._mfax_faxroutegetroutinginfo, faxroute/FaxRouteGetRoutingInfo
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
 - FaxRouteGetRoutingInfo
 - faxroute/FaxRouteGetRoutingInfo
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
 - FaxRouteGetRoutingInfo
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

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The fax service calls the <b>FaxRouteGetRoutingInfo</b> function twice. On the first call to the function the fax service passes a null pointer in the <i>RoutingInfo</i> parameter. The fax routing extension DLL must set the <i>RoutingInfoSize</i> parameter to the size required for the <i>RoutingInfo</i> buffer. The fax service calls <b>FaxRouteGetRoutingInfo</b> a second time with a valid pointer to the <i>RoutingInfo</i> buffer.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-routing-extension-api">Fax Routing Extension Application Programming Interface Overview</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-routing-extension-functions">Fax Routing Extension Functions</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nf-faxroute-faxroutesetroutinginfo">FaxRouteSetRoutingInfo</a>