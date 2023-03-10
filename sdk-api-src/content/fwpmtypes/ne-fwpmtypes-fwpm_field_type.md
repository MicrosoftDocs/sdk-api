---
UID: NE:fwpmtypes.FWPM_FIELD_TYPE_
title: FWPM_FIELD_TYPE (fwpmtypes.h)
description: Provides additional information about how the field's data should be interpreted.
helpviewer_keywords: ["FWPM_FIELD_FLAGS","FWPM_FIELD_IP_ADDRESS","FWPM_FIELD_RAW_DATA","FWPM_FIELD_TYPE","FWPM_FIELD_TYPE enumeration [Filtering]","FWPM_FIELD_TYPE_MAX","fwp.fwpm_field_type_enum","fwpmtypes/FWPM_FIELD_FLAGS","fwpmtypes/FWPM_FIELD_IP_ADDRESS","fwpmtypes/FWPM_FIELD_RAW_DATA","fwpmtypes/FWPM_FIELD_TYPE","fwpmtypes/FWPM_FIELD_TYPE_MAX"]
old-location: fwp\fwpm_field_type_enum.htm
tech.root: fwp
ms.assetid: 46983847-7c68-4ee7-946e-ea62f34d1a38
ms.date: 12/05/2018
ms.keywords: FWPM_FIELD_FLAGS, FWPM_FIELD_IP_ADDRESS, FWPM_FIELD_RAW_DATA, FWPM_FIELD_TYPE, FWPM_FIELD_TYPE enumeration [Filtering], FWPM_FIELD_TYPE_MAX, fwp.fwpm_field_type_enum, fwpmtypes/FWPM_FIELD_FLAGS, fwpmtypes/FWPM_FIELD_IP_ADDRESS, fwpmtypes/FWPM_FIELD_RAW_DATA, fwpmtypes/FWPM_FIELD_TYPE, fwpmtypes/FWPM_FIELD_TYPE_MAX
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FWPM_FIELD_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_FIELD_TYPE_
 - fwpmtypes/FWPM_FIELD_TYPE_
 - FWPM_FIELD_TYPE
 - fwpmtypes/FWPM_FIELD_TYPE
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
 - FWPM_FIELD_TYPE
---

# FWPM_FIELD_TYPE enumeration


## -description

The <b>FWPM_FIELD_TYPE</b> enumerated type provides additional information about how the field's data should be
interpreted.

## -enum-fields

### -field FWPM_FIELD_RAW_DATA:0

Value contains raw data.

### -field FWPM_FIELD_IP_ADDRESS

Value contains an IP address.

### -field FWPM_FIELD_FLAGS

Value contains flags.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field FWPM_FIELD_TYPE_MAX

Maximum value for testing purposes.

