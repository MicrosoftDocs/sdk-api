---
UID: NS:fwpmtypes.FWPM_FIELD0_
title: FWPM_FIELD0_
author: windows-sdk-content
description: Specifies schema information for a field.
old-location: fwp\fwpm_field0_struct.htm
tech.root: fwp
ms.assetid: 30d68d48-156e-440b-8607-8b64cfa25049
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: FWPM_FIELD0, FWPM_FIELD0 structure [Filtering], FWPM_FIELD0_, fwp.fwpm_field0_struct, fwpmtypes/FWPM_FIELD0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: FWPM_FIELD0
req.redist: 
---

# FWPM_FIELD0_ structure


## -description


The <b>FWPM_FIELD0</b> structure specifies schema information for a field. 


## -struct-fields




### -field fieldKey

Uniquely identifies the field. See FWPM_CONDITION_* identifiers in the topic <a href="https://msdn.microsoft.com/4f0b970a-e511-4107-8023-22a8775905b9">Filtering Condition Identifiers</a>.


### -field type

Determines how <b>dataType</b> is interpreted.

See <a href="https://msdn.microsoft.com/46983847-7c68-4ee7-946e-ea62f34d1a38">FWPM_FIELD_TYPE</a> for more information.


### -field dataType

Data type passed to classify.

See <a href="https://msdn.microsoft.com/db605170-bfe0-4339-8a40-7b1ce435278b">FWP_DATA_TYPE</a> for more information.


## -remarks



<b>FWPM_FIELD0</b> is a specific implementation of FWPM_FIELD. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/46983847-7c68-4ee7-946e-ea62f34d1a38">FWPM_FIELD_TYPE</a>



<a href="https://msdn.microsoft.com/db605170-bfe0-4339-8a40-7b1ce435278b">FWP_DATA_TYPE</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

