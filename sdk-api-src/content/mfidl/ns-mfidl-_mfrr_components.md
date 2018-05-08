---
UID: NS:mfidl._MFRR_COMPONENTS
title: "_MFRR_COMPONENTS"
author: windows-driver-content
description: Contains information about one or more revoked components.
old-location: mf\mfrr_components.htm
old-project: medfound
ms.assetid: df12e64b-92e3-4446-bade-3ad55cbedf51
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: "*PMFRR_COMPONENTS, MFRR_COMPONENTS, MFRR_COMPONENTS structure [Media Foundation], PMFRR_COMPONENTS, PMFRR_COMPONENTS structure pointer [Media Foundation], _MFRR_COMPONENTS, df12e64b-92e3-4446-bade-3ad55cbedf51, mf.mfrr_components, mfidl/MFRR_COMPONENTS, mfidl/PMFRR_COMPONENTS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mfidl.h
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
req.typenames: MFRR_COMPONENTS, *PMFRR_COMPONENTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfidl.h
api_name:
-	MFRR_COMPONENTS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MFRR_COMPONENTS structure


## -description



Contains information about one or more revoked components.




## -struct-fields




### -field dwRRInfoVersion

Revocation information version.


### -field dwRRComponents

Number of elements in the <b>pRRComponents</b> array.


### -field pRRComponents

Array of <a href="https://msdn.microsoft.com/e23bc68c-b62e-4483-b2a7-a7de7376697f">MFRR_COMPONENT_HASH_INFO</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/e23bc68c-b62e-4483-b2a7-a7de7376697f">MFRR_COMPONENT_HASH_INFO</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

