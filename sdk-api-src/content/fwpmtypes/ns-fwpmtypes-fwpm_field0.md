---
UID: NS:fwpmtypes.FWPM_FIELD0_
title: FWPM_FIELD0 (fwpmtypes.h)
author: windows-sdk-content
description: Specifies schema information for a field.
old-location: fwp\fwpm_field0_struct.htm
tech.root: fwp
ms.assetid: 30d68d48-156e-440b-8607-8b64cfa25049
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FWPM_FIELD0, FWPM_FIELD0 structure [Filtering], FWPM_FIELD0_, fwp.fwpm_field0_struct, fwpmtypes/FWPM_FIELD0
ms.topic: struct
f1_keywords: 
 - "fwpmtypes/FWPM_FIELD0"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_FIELD0
targetos: Windows
req.typenames: FWPM_FIELD0
req.redist: 
ms.custom: 19H1
---

# FWPM_FIELD0 structure


## -description


The <b>FWPM_FIELD0</b> structure specifies schema information for a field. 


## -struct-fields




### -field fieldKey

Uniquely identifies the field. See FWPM_CONDITION_* identifiers in the topic <a href="https://docs.microsoft.com/windows/desktop/FWP/filtering-condition-identifiers-">Filtering Condition Identifiers</a>.


### -field type

Determines how <b>dataType</b> is interpreted.

See <a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_field_type_">FWPM_FIELD_TYPE</a> for more information.


### -field dataType

Data type passed to classify.

See <a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_data_type_">FWP_DATA_TYPE</a> for more information.


## -remarks



<b>FWPM_FIELD0</b> is a specific implementation of FWPM_FIELD. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_field_type_">FWPM_FIELD_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_data_type_">FWP_DATA_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

