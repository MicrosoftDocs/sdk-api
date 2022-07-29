---
UID: NS:fwpmtypes.FWPM_CONNECTION_SUBSCRIPTION0_
title: FWPM_CONNECTION_SUBSCRIPTION0 (fwpmtypes.h)
description: Stores information used to subscribe to notifications about a connection object.
helpviewer_keywords: ["FWPM_CONNECTION_SUBSCRIPTION0","FWPM_CONNECTION_SUBSCRIPTION0 structure [Filtering]","fwp.fwpm_connection_subscription0","fwpmtypes/FWPM_CONNECTION_SUBSCRIPTION0"]
old-location: fwp\fwpm_connection_subscription0.htm
tech.root: fwp
ms.assetid: 020490f1-ccbe-41aa-b6ad-022be9c9bef4
ms.date: 12/05/2018
ms.keywords: FWPM_CONNECTION_SUBSCRIPTION0, FWPM_CONNECTION_SUBSCRIPTION0 structure [Filtering], fwp.fwpm_connection_subscription0, fwpmtypes/FWPM_CONNECTION_SUBSCRIPTION0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_CONNECTION_SUBSCRIPTION0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_CONNECTION_SUBSCRIPTION0_
 - fwpmtypes/FWPM_CONNECTION_SUBSCRIPTION0_
 - FWPM_CONNECTION_SUBSCRIPTION0
 - fwpmtypes/FWPM_CONNECTION_SUBSCRIPTION0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_CONNECTION_SUBSCRIPTION0
---

# FWPM_CONNECTION_SUBSCRIPTION0 structure


## -description

The <b>FWPM_CONNECTION_SUBSCRIPTION0</b> structure stores information used to subscribe to notifications about a connection object.

## -struct-fields

### -field enumTemplate

Type: **[FWPM_CONNECTION_ENUM_TEMPLATE0](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)**

Enumeration template for limiting the subscription.

### -field flags

Reserved for system use.

### -field sessionKey

Identifies the session that created the subscription.

## -see-also

[FWPM_CONNECTION_ENUM_TEMPLATE0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
