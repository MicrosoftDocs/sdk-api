---
UID: NS:winsvc._ENUM_SERVICE_STATUSA
title: ENUM_SERVICE_STATUSA (winsvc.h)
description: Contains the name of a service in a service control manager database and information about that service. It is used by the EnumDependentServices and EnumServicesStatus functions. (ANSI)
helpviewer_keywords: ["*LPENUM_SERVICE_STATUSA","ENUM_SERVICE_STATUS","ENUM_SERVICE_STATUS structure","ENUM_SERVICE_STATUSA","ENUM_SERVICE_STATUSW","LPENUM_SERVICE_STATUS","LPENUM_SERVICE_STATUS structure pointer","_win32_enum_service_status_str","base.enum_service_status_str","winsvc/ENUM_SERVICE_STATUS","winsvc/ENUM_SERVICE_STATUSA","winsvc/ENUM_SERVICE_STATUSW","winsvc/LPENUM_SERVICE_STATUS"]
old-location: base\enum_service_status_str.htm
tech.root: security
ms.assetid: b088bd94-5d25-44a7-93c0-80ce6588b811
ms.date: 12/05/2018
ms.keywords: '*LPENUM_SERVICE_STATUSA, ENUM_SERVICE_STATUS, ENUM_SERVICE_STATUS structure, ENUM_SERVICE_STATUSA, ENUM_SERVICE_STATUSW, LPENUM_SERVICE_STATUS, LPENUM_SERVICE_STATUS structure pointer, _win32_enum_service_status_str, base.enum_service_status_str, winsvc/ENUM_SERVICE_STATUS, winsvc/ENUM_SERVICE_STATUSA, winsvc/ENUM_SERVICE_STATUSW, winsvc/LPENUM_SERVICE_STATUS'
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ENUM_SERVICE_STATUSW (Unicode) and ENUM_SERVICE_STATUSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ENUM_SERVICE_STATUSA, *LPENUM_SERVICE_STATUSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENUM_SERVICE_STATUSA
 - winsvc/_ENUM_SERVICE_STATUSA
 - LPENUM_SERVICE_STATUSA
 - winsvc/LPENUM_SERVICE_STATUSA
 - ENUM_SERVICE_STATUSA
 - winsvc/ENUM_SERVICE_STATUSA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsvc.h
api_name:
 - ENUM_SERVICE_STATUS
 - ENUM_SERVICE_STATUSA
 - ENUM_SERVICE_STATUSW
---

# ENUM_SERVICE_STATUSA structure


## -description

Contains the name of a service in a service control manager database and information about that service. It is used by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-enumdependentservicesa">EnumDependentServices</a> and 
<a href="/windows/desktop/api/winsvc/nf-winsvc-enumservicesstatusa">EnumServicesStatus</a> functions.

## -struct-fields

### -field lpServiceName

The name of a service in the service control manager database. The maximum string length is 256 characters. The service control manager database preserves the case of the characters, but service name comparisons are always case insensitive. A slash (/), backslash (\\), comma, and space are invalid service name characters.

### -field lpDisplayName

A display name that can be used by service control programs, such as Services in Control Panel, to identify the service. This string has a maximum length of 256 characters. The name is case-preserved in the service control manager. Display name comparisons are always case-insensitive.

### -field ServiceStatus

A 
<a href="/windows/desktop/api/winsvc/ns-winsvc-service_status">SERVICE_STATUS</a> structure that contains status information for the <b>lpServiceName</b> service.

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-enumdependentservicesa">EnumDependentServices</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-enumservicesstatusa">EnumServicesStatus</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_status">SERVICE_STATUS</a>

## -remarks

> [!NOTE]
> The winsvc.h header defines ENUM_SERVICE_STATUS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
