---
UID: NE:wbemcli.tag_WBEM_CONNECT_OPTIONS
title: WBEM_CONNECT_OPTIONS (wbemcli.h)
description: Contains flags for the IWbemLocator::ConnectServer method.
helpviewer_keywords: ["WBEM_CONNECT_OPTIONS","WBEM_CONNECT_OPTIONS enumeration [Windows Management Instrumentation]","WBEM_FLAG_CONNECT_PROVIDERS","WBEM_FLAG_CONNECT_REPOSITORY_ONLY","WBEM_FLAG_CONNECT_USE_MAX_WAIT","wbemcli/WBEM_CONNECT_OPTIONS","wbemcli/WBEM_FLAG_CONNECT_PROVIDERS","wbemcli/WBEM_FLAG_CONNECT_REPOSITORY_ONLY","wbemcli/WBEM_FLAG_CONNECT_USE_MAX_WAIT","wmi.wbem_connect_options"]
old-location: wmi\wbem_connect_options.htm
tech.root: wmi
ms.assetid: 8D6FA5C1-B10B-48C6-A0E9-8F7D6C07B957
ms.date: 12/05/2018
ms.keywords: WBEM_CONNECT_OPTIONS, WBEM_CONNECT_OPTIONS enumeration [Windows Management Instrumentation], WBEM_FLAG_CONNECT_PROVIDERS, WBEM_FLAG_CONNECT_REPOSITORY_ONLY, WBEM_FLAG_CONNECT_USE_MAX_WAIT, wbemcli/WBEM_CONNECT_OPTIONS, wbemcli/WBEM_FLAG_CONNECT_PROVIDERS, wbemcli/WBEM_FLAG_CONNECT_REPOSITORY_ONLY, wbemcli/WBEM_FLAG_CONNECT_USE_MAX_WAIT, wmi.wbem_connect_options
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
req.typenames: WBEM_CONNECT_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_WBEM_CONNECT_OPTIONS
 - wbemcli/tag_WBEM_CONNECT_OPTIONS
 - WBEM_CONNECT_OPTIONS
 - wbemcli/WBEM_CONNECT_OPTIONS
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - WBEM_CONNECT_OPTIONS
---

# WBEM_CONNECT_OPTIONS enumeration


## -description

Contains flags for the <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemlocator-connectserver">IWbemLocator::ConnectServer</a> method.

## -enum-fields

### -field WBEM_FLAG_CONNECT_REPOSITORY_ONLY:0x40

Reserved for internal use. Do not use.

### -field WBEM_FLAG_CONNECT_USE_MAX_WAIT:0x80

The call  returns in 2 minutes or less whether successful or not.

### -field WBEM_FLAG_CONNECT_PROVIDERS:0x100

TBD
