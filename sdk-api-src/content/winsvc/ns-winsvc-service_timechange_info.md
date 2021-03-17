---
UID: NS:winsvc._SERVICE_TIMECHANGE_INFO
title: SERVICE_TIMECHANGE_INFO (winsvc.h)
description: Contains system time change settings.
helpviewer_keywords: ["*PSERVICE_TIMECHANGE_INFO","PSERVICE_TIMECHANGE_INFO","PSERVICE_TIMECHANGE_INFO structure pointer","SERVICE_TIMECHANGE_INFO","SERVICE_TIMECHANGE_INFO structure","base.service_timechange_info","winsvc/PSERVICE_TIMECHANGE_INFO","winsvc/SERVICE_TIMECHANGE_INFO"]
old-location: base\service_timechange_info.htm
tech.root: security
ms.assetid: 452b0678-dfea-4128-9236-273323b519f0
ms.date: 12/05/2018
ms.keywords: '*PSERVICE_TIMECHANGE_INFO, PSERVICE_TIMECHANGE_INFO, PSERVICE_TIMECHANGE_INFO structure pointer, SERVICE_TIMECHANGE_INFO, SERVICE_TIMECHANGE_INFO structure, base.service_timechange_info, winsvc/PSERVICE_TIMECHANGE_INFO, winsvc/SERVICE_TIMECHANGE_INFO'
req.header: winsvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: SERVICE_TIMECHANGE_INFO, *PSERVICE_TIMECHANGE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_TIMECHANGE_INFO
 - winsvc/_SERVICE_TIMECHANGE_INFO
 - PSERVICE_TIMECHANGE_INFO
 - winsvc/PSERVICE_TIMECHANGE_INFO
 - SERVICE_TIMECHANGE_INFO
 - winsvc/SERVICE_TIMECHANGE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsvc.h
api_name:
 - SERVICE_TIMECHANGE_INFO
---

# SERVICE_TIMECHANGE_INFO structure


## -description

Contains system time change settings.

## -struct-fields

### -field liNewTime

The new system time.

### -field liOldTime

The previous system time.

## -remarks

The time values in the <i>liNewTime</i> and <i>liOldTime</i> members cannot be used directly with the time functions, which typically require a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> or <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure. Convert the  <a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a> structure to a  <a href="/windows/win32/api/winnt/ns-winnt-ularge_integer~r1">ULARGE_INTEGER</a> structure, copy the <b>ULARGE_INTEGER</b> structure to a <b>FILETIME</b> structure, and then if necessary use the <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-filetimetosystemtime">FileTimeToSystemTime</a> function to convert the <b>FILETIME</b> structure to a <b>SYSTEMTIME</b> structure.

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfig2a">QueryServiceConfig2</a>