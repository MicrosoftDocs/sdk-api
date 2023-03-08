---
UID: NS:windns._DNS_APPLICATION_SETTINGS
title: DNS_APPLICATION_SETTINGS
description: Represents per-application DNS settings.
tech.root: DNS
ms.date: 08/31/2021
req.construct-type: structure
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
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
req.typenames: DNS_APPLICATION_SETTINGS
req.redist: 
f1_keywords:
 - _DNS_APPLICATION_SETTINGS
 - windns/_DNS_APPLICATION_SETTINGS
 - DNS_APPLICATION_SETTINGS
 - windns/DNS_APPLICATION_SETTINGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - windns.h
api_name:
 - _DNS_APPLICATION_SETTINGS
 - DNS_APPLICATION_SETTINGS
prerelease: false
---

## -description

Represents per-application DNS settings.

## -struct-fields

### -field Version

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

Must be set to **DNS_APP_SETTINGS_VERSION1**.

### -field Flags

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

A bitset containing the following options.

* **DNS_APP_SETTINGS_EXCLUSIVE_SERVERS** (0x1). Use the custom DNS servers exclusively, and don't try the system-configured ones.

## -remarks

## -see-also
