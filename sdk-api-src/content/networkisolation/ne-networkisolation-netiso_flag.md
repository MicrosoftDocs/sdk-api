---
UID: NE:networkisolation.NETISO_FLAG
title: NETISO_FLAG (networkisolation.h)
description: Specifies whether binaries should be returned for app containers.
helpviewer_keywords: ["NETISO_FLAG","NETISO_FLAG enumeration [ICS/ICF]","NETISO_FLAG_FORCE_COMPUTE_BINARIES","NETISO_FLAG_MAX","ics.netiso_flag","networkisolation/NETISO_FLAG","networkisolation/NETISO_FLAG_FORCE_COMPUTE_BINARIES","networkisolation/NETISO_FLAG_MAX"]
old-location: ics\netiso_flag.htm
tech.root: ics
ms.assetid: 0e07c3ed-0561-453d-b92a-cd0db07ea5cf
ms.date: 12/05/2018
ms.keywords: NETISO_FLAG, NETISO_FLAG enumeration [ICS/ICF], NETISO_FLAG_FORCE_COMPUTE_BINARIES, NETISO_FLAG_MAX, ics.netiso_flag, networkisolation/NETISO_FLAG, networkisolation/NETISO_FLAG_FORCE_COMPUTE_BINARIES, networkisolation/NETISO_FLAG_MAX
req.header: networkisolation.h
req.include-header: Netfw.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: NETISO_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NETISO_FLAG
 - networkisolation/NETISO_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - networkisolation.h
api_name:
 - NETISO_FLAG
---

# NETISO_FLAG enumeration


## -description

The <b>NETISO_FLAG</b> enumerated type specifies whether binaries should be returned for app containers.

## -enum-fields

### -field NETISO_FLAG_FORCE_COMPUTE_BINARIES:0x1

Specifies that all binaries will be computed before the app container is returned.

This flag should be set if the caller requires up-to-date and complete information on app container binaries. If this flag is not set, returned data may be stale or incomplete.

### -field NETISO_FLAG_MAX:0x2

Maximum value for testing purposes.

## -remarks

By default, binaries are not returned. <b>NETISO_FLAG_FORCE_COMPUTE_BINARIES</b> must be set in order for these to be returned.

