---
UID: NE:avrfsdk.eAvrfResourceTypes
title: eAvrfResourceTypes (avrfsdk.h)
description: Specifies the types of resources that can be enumerated using the VerifierEnumerateResource function.
old-location: winprog\eavrfresourcetypes.htm
tech.root: DevNotes
ms.assetid: 6887e584-0d0f-45ca-b926-47a55f19c9a2
ms.date: 12/05/2018
ms.keywords: AvrfResourceHandleTrace, AvrfResourceHeapAllocation, AvrfResourceMax, avrfsdk/AvrfResourceHandleTrace, avrfsdk/AvrfResourceHeapAllocation, avrfsdk/AvrfResourceMax, avrfsdk/eAvrfResourceTypes, base.eavrfresourcetypes, eAvrfResourceTypes, eAvrfResourceTypes enumeration [Windows API], winprog.eavrfresourcetypes
ms.topic: enum
f1_keywords:
- avrfsdk/eAvrfResourceTypes
dev_langs:
- c++
req.header: avrfsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- Avrfsdk.h
api_name:
- eAvrfResourceTypes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# eAvrfResourceTypes enumeration


## -description


Specifies the types of resources that can be enumerated using the <a href="https://docs.microsoft.com/windows/desktop/api/avrfsdk/nf-avrfsdk-verifierenumerateresource">VerifierEnumerateResource</a> function.


## -enum-fields




### -field AvrfResourceHeapAllocation

Indicates heap-allocation information is being obtained.


### -field AvrfResourceHandleTrace

Indicates handle trace information is being obtained.


### -field AvrfResourceMax

Indicates the upper boundary of the current implementation's resource type.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DevNotes/resource-enumeration">Resource Enumeration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/avrfsdk/nf-avrfsdk-verifierenumerateresource">VerifierEnumerateResource</a>
 

 

