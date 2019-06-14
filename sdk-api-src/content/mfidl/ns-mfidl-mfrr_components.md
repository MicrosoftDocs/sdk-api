---
UID: NS:mfidl._MFRR_COMPONENTS
title: MFRR_COMPONENTS (mfidl.h)
author: windows-sdk-content
description: Contains information about one or more revoked components.
old-location: mf\mfrr_components.htm
tech.root: medfound
ms.assetid: df12e64b-92e3-4446-bade-3ad55cbedf51
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PMFRR_COMPONENTS, MFRR_COMPONENTS, MFRR_COMPONENTS structure [Media Foundation], PMFRR_COMPONENTS, PMFRR_COMPONENTS structure pointer [Media Foundation], df12e64b-92e3-4446-bade-3ad55cbedf51, mf.mfrr_components, mfidl/MFRR_COMPONENTS, mfidl/PMFRR_COMPONENTS"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFRR_COMPONENTS
product: Windows
targetos: Windows
req.typenames: MFRR_COMPONENTS, *PMFRR_COMPONENTS
req.redist: 
ms.custom: 19H1
---

# MFRR_COMPONENTS structure


## -description



Contains information about one or more revoked components.




## -struct-fields




### -field dwRRInfoVersion

Revocation information version.


### -field dwRRComponents

Number of elements in the <b>pRRComponents</b> array.


### -field pRRComponents

Array of <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/ns-mfidl-_mfrr_component_hash_info">MFRR_COMPONENT_HASH_INFO</a> structures.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/ns-mfidl-_mfrr_component_hash_info">MFRR_COMPONENT_HASH_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>
 

 

