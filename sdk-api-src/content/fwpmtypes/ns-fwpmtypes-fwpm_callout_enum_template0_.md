---
UID: NS:fwpmtypes.FWPM_CALLOUT_ENUM_TEMPLATE0_
title: FWPM_CALLOUT_ENUM_TEMPLATE0_
author: windows-sdk-content
description: Used for limiting callout enumerations.
old-location: fwp\fwpm_callout_enum_template0_struct.htm
tech.root: fwp
ms.assetid: 10997be6-069d-4d1a-a6b1-1a1e0a5359c5
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: FWPM_CALLOUT_ENUM_TEMPLATE0, FWPM_CALLOUT_ENUM_TEMPLATE0 structure [Filtering], FWPM_CALLOUT_ENUM_TEMPLATE0_, fwp.fwpm_callout_enum_template0_struct, fwpmtypes/FWPM_CALLOUT_ENUM_TEMPLATE0
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - FWPM_CALLOUT_ENUM_TEMPLATE0
product: Windows
targetos: Windows
req.typenames: FWPM_CALLOUT_ENUM_TEMPLATE0
req.redist: 
---

# FWPM_CALLOUT_ENUM_TEMPLATE0_ structure


## -description


The <b>FWPM_CALLOUT_ENUM_TEMPLATE0</b> structure is used for limiting callout enumerations.


## -struct-fields




### -field providerKey

Uniquely identifies the provider associated with the callout. If this member is non-NULL, only objects associated with the specified provider will be returned.


### -field layerKey

Uniquely identifies a layer. If this member is non-NULL, only callouts associated with the specified layer will be returned.


## -remarks



<b>FWPM_CALLOUT_ENUM_TEMPLATE0</b> is a specific implementation of FWPM_CALLOUT_ENUM_TEMPLATE. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

