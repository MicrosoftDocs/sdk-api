---
UID: NS:winsvc._ENUM_SERVICE_STATUSW
title: ENUM_SERVICE_STATUSW (winsvc.h)
author: windows-sdk-content
description: Contains the name of a service in a service control manager database and information about that service. It is used by the EnumDependentServices and EnumServicesStatus functions.
old-location: base\enum_service_status_str.htm
tech.root: Services
ms.assetid: b088bd94-5d25-44a7-93c0-80ce6588b811
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*LPENUM_SERVICE_STATUSW, ENUM_SERVICE_STATUS, ENUM_SERVICE_STATUS structure, ENUM_SERVICE_STATUSA, ENUM_SERVICE_STATUSW, LPENUM_SERVICE_STATUS, LPENUM_SERVICE_STATUS structure pointer, _win32_enum_service_status_str, base.enum_service_status_str, winsvc/ENUM_SERVICE_STATUS, winsvc/ENUM_SERVICE_STATUSA, winsvc/ENUM_SERVICE_STATUSW, winsvc/LPENUM_SERVICE_STATUS'
ms.topic: struct
f1_keywords:
- winsvc/ENUM_SERVICE_STATUS
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
product: Windows
targetos: Windows
req.typenames: ENUM_SERVICE_STATUSW, *LPENUM_SERVICE_STATUSW
req.redist: 
ms.custom: 19H1
---

# ENUM_SERVICE_STATUSW structure


## -description


Contains the name of a service in a service control manager database and information about that service. It is used by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nf-winsvc-enumdependentservicesa">EnumDependentServices</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nf-winsvc-enumservicesstatusa">EnumServicesStatus</a> functions.


## -struct-fields




### -field lpServiceName

The name of a service in the service control manager database. The maximum string length is 256 characters. The service control manager database preserves the case of the characters, but service name comparisons are always case insensitive. A slash (/), backslash (\), comma, and space are invalid service name characters.


### -field lpDisplayName

A display name that can be used by service control programs, such as Services in Control Panel, to identify the service. This string has a maximum length of 256 characters. The name is case-preserved in the service control manager. Display name comparisons are always case-insensitive.


### -field ServiceStatus

A 
<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/ns-winsvc-service_status">SERVICE_STATUS</a> structure that contains status information for the <b>lpServiceName</b> service.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nf-winsvc-enumdependentservicesa">EnumDependentServices</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nf-winsvc-enumservicesstatusa">EnumServicesStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/ns-winsvc-service_status">SERVICE_STATUS</a>
 

 

