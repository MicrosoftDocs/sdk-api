---
UID: NE:wbemcli.tag_WBEM_STATUS_TYPE
title: WBEM_STATUS_TYPE (wbemcli.h)
description: Describes the status of an asynchronous operation.
helpviewer_keywords: ["WBEM_STATUS_COMPLETE","WBEM_STATUS_LOGGING_INFORMATION","WBEM_STATUS_LOGGING_INFORMATION_ESS","WBEM_STATUS_LOGGING_INFORMATION_HOST","WBEM_STATUS_LOGGING_INFORMATION_PROVIDER","WBEM_STATUS_LOGGING_INFORMATION_REPOSITORY","WBEM_STATUS_PROGRESS","WBEM_STATUS_REQUIREMENTS","WBEM_STATUS_TYPE","WBEM_STATUS_TYPE enumeration [Windows Management Instrumentation]","wbemcli/WBEM_STATUS_COMPLETE","wbemcli/WBEM_STATUS_LOGGING_INFORMATION","wbemcli/WBEM_STATUS_LOGGING_INFORMATION_ESS","wbemcli/WBEM_STATUS_LOGGING_INFORMATION_HOST","wbemcli/WBEM_STATUS_LOGGING_INFORMATION_PROVIDER","wbemcli/WBEM_STATUS_LOGGING_INFORMATION_REPOSITORY","wbemcli/WBEM_STATUS_PROGRESS","wbemcli/WBEM_STATUS_REQUIREMENTS","wbemcli/WBEM_STATUS_TYPE","wmi.wbem_status_type"]
old-location: wmi\wbem_status_type.htm
tech.root: wmi
ms.assetid: 3AD9FAB6-57A3-4BD8-8E13-6BEF0868681A
ms.date: 12/05/2018
ms.keywords: WBEM_STATUS_COMPLETE, WBEM_STATUS_LOGGING_INFORMATION, WBEM_STATUS_LOGGING_INFORMATION_ESS, WBEM_STATUS_LOGGING_INFORMATION_HOST, WBEM_STATUS_LOGGING_INFORMATION_PROVIDER, WBEM_STATUS_LOGGING_INFORMATION_REPOSITORY, WBEM_STATUS_PROGRESS, WBEM_STATUS_REQUIREMENTS, WBEM_STATUS_TYPE, WBEM_STATUS_TYPE enumeration [Windows Management Instrumentation], wbemcli/WBEM_STATUS_COMPLETE, wbemcli/WBEM_STATUS_LOGGING_INFORMATION, wbemcli/WBEM_STATUS_LOGGING_INFORMATION_ESS, wbemcli/WBEM_STATUS_LOGGING_INFORMATION_HOST, wbemcli/WBEM_STATUS_LOGGING_INFORMATION_PROVIDER, wbemcli/WBEM_STATUS_LOGGING_INFORMATION_REPOSITORY, wbemcli/WBEM_STATUS_PROGRESS, wbemcli/WBEM_STATUS_REQUIREMENTS, wbemcli/WBEM_STATUS_TYPE, wmi.wbem_status_type
req.header: wbemcli.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: WBEM_STATUS_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_WBEM_STATUS_TYPE
 - wbemcli/tag_WBEM_STATUS_TYPE
 - WBEM_STATUS_TYPE
 - wbemcli/WBEM_STATUS_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemcli.h
api_name:
 - WBEM_STATUS_TYPE
---

# WBEM_STATUS_TYPE enumeration


## -description

Describes the status of an asynchronous operation.

## -enum-fields

### -field WBEM_STATUS_COMPLETE:0

The operation has completed.

### -field WBEM_STATUS_REQUIREMENTS:1

Used in activating post-filtering.

### -field WBEM_STATUS_PROGRESS:2

The operation is still in progress.

### -field WBEM_STATUS_LOGGING_INFORMATION:0x100

Reserved for future use.

### -field WBEM_STATUS_LOGGING_INFORMATION_PROVIDER:0x200

Reserved for future use.

### -field WBEM_STATUS_LOGGING_INFORMATION_HOST:0x400

Reserved for future use.

### -field WBEM_STATUS_LOGGING_INFORMATION_REPOSITORY:0x800

Reserved for future use.

### -field WBEM_STATUS_LOGGING_INFORMATION_ESS:0x1000

Reserved for future use.

## -see-also

<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync">IWbemServices::ExecQueryAsync</a>
