---
UID: NE:fwpmtypes.FWPM_FIELD_TYPE_
title: FWPM_FIELD_TYPE_
author: windows-sdk-content
description: Provides additional information about how the field's data should be interpreted.
old-location: fwp\fwpm_field_type_enum.htm
old-project: fwp
ms.assetid: 46983847-7c68-4ee7-946e-ea62f34d1a38
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: FWPM_FIELD_FLAGS, FWPM_FIELD_IP_ADDRESS, FWPM_FIELD_RAW_DATA, FWPM_FIELD_TYPE, FWPM_FIELD_TYPE enumeration [Filtering], FWPM_FIELD_TYPE_, FWPM_FIELD_TYPE_MAX, fwp.fwpm_field_type_enum, fwpmtypes/FWPM_FIELD_FLAGS, fwpmtypes/FWPM_FIELD_IP_ADDRESS, fwpmtypes/FWPM_FIELD_RAW_DATA, fwpmtypes/FWPM_FIELD_TYPE, fwpmtypes/FWPM_FIELD_TYPE_MAX
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FWPM_FIELD_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_FIELD_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_FIELD_TYPE_ enumeration


## -description



		The <b>FWPM_FIELD_TYPE</b> enumerated type provides additional information about how the field's data should be
interpreted.


## -enum-fields




### -field FWPM_FIELD_RAW_DATA

Value contains raw data.


### -field FWPM_FIELD_IP_ADDRESS

Value contains an IP address.


### -field FWPM_FIELD_FLAGS

Value contains flags.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field FWPM_FIELD_TYPE_MAX

Maximum value for testing purposes.

