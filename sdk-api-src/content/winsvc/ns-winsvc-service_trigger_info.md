---
UID: NS:winsvc._SERVICE_TRIGGER_INFO
title: SERVICE_TRIGGER_INFO (winsvc.h)
description: Contains trigger event information for a service. This structure is used by the ChangeServiceConfig2 and QueryServiceConfig2 functions.
helpviewer_keywords: ["*PSERVICE_TRIGGER_INFO","PSERVICE_TRIGGER_INFO","PSERVICE_TRIGGER_INFO structure pointer","SERVICE_TRIGGER_INFO","SERVICE_TRIGGER_INFO structure","base.service_trigger_info","winsvc/PSERVICE_TRIGGER_INFO","winsvc/SERVICE_TRIGGER_INFO"]
old-location: base\service_trigger_info.htm
tech.root: security
ms.assetid: 8de46056-1ea5-46f2-a260-ad140fd77bc1
ms.date: 12/05/2018
ms.keywords: '*PSERVICE_TRIGGER_INFO, PSERVICE_TRIGGER_INFO, PSERVICE_TRIGGER_INFO structure pointer, SERVICE_TRIGGER_INFO, SERVICE_TRIGGER_INFO structure, base.service_trigger_info, winsvc/PSERVICE_TRIGGER_INFO, winsvc/SERVICE_TRIGGER_INFO'
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
req.typenames: SERVICE_TRIGGER_INFO, *PSERVICE_TRIGGER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_TRIGGER_INFO
 - winsvc/_SERVICE_TRIGGER_INFO
 - PSERVICE_TRIGGER_INFO
 - winsvc/PSERVICE_TRIGGER_INFO
 - SERVICE_TRIGGER_INFO
 - winsvc/SERVICE_TRIGGER_INFO
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
 - SERVICE_TRIGGER_INFO
---

# SERVICE_TRIGGER_INFO structure


## -description

Contains trigger event information for a service. This structure is used by the <a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a> and <a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfig2a">QueryServiceConfig2</a> functions.

## -struct-fields

### -field cTriggers

The number of triggers in the array of <a href="/windows/desktop/api/winsvc/ns-winsvc-service_trigger">SERVICE_TRIGGER</a> structures pointed to by the <b>pTriggers</b> member.  

If this member is 0 in a <b>SERVICE_TRIGGER_INFO</b> structure passed to  <a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>, all previously configured triggers are removed from the service. If the service has no triggers configured, <b>ChangeServiceConfig2</b>  fails with ERROR_INVALID_PARAMETER.

### -field cTriggers.range

### -field cTriggers.range.0

### -field cTriggers.range.64

### -field pTriggers

A pointer to an array of <a href="/windows/desktop/api/winsvc/ns-winsvc-service_trigger">SERVICE_TRIGGER</a> structures that specify the trigger events for the service. If the <b>cTriggers</b> member is 0, this member is not used.

### -field pTriggers.size_is

### -field pTriggers.size_is.cTriggers

### -field pReserved

This member is reserved and must be NULL.

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfig2a">QueryServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_trigger">SERVICE_TRIGGER</a>



<a href="/windows/desktop/Services/service-trigger-events">Service Trigger Events</a>