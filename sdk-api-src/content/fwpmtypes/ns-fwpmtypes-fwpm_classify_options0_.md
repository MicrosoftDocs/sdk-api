---
UID: NS:fwpmtypes.FWPM_CLASSIFY_OPTIONS0_
title: FWPM_CLASSIFY_OPTIONS0_
author: windows-driver-content
description: The FWPM_CLASSIFY_OPTIONS0 structure is used to store FWPM_CLASSIFY_OPTION0 structures.
old-location: fwp\fwpm_classify_options0.htm
old-project: FWP
ms.assetid: 5d1f7807-4188-4a57-83fc-99683254e3a5
ms.author: windowsdriverdev
ms.date: 4/12/2018
ms.keywords: FWPM_CLASSIFY_OPTIONS0, FWPM_CLASSIFY_OPTIONS0 structure [Filtering], FWPM_CLASSIFY_OPTIONS0_, fwp.fwpm_classify_options0, fwpmtypes/FWPM_CLASSIFY_OPTIONS0
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
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FWPM_CLASSIFY_OPTIONS0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Fwpmtypes.h
api_name:
-	FWPM_CLASSIFY_OPTIONS0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_CLASSIFY_OPTIONS0_ structure


## -description


 The <b>FWPM_CLASSIFY_OPTIONS0</b> structure is used to store <b>FWPM_CLASSIFY_OPTION0</b> structures.


## -struct-fields




### -field numOptions

Number of <b>FWPM_CLASSIFY_OPTION0</b> structures in the <b>options</b> member.


### -field options

[size_is(numCredentials)]

Pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff550078">FWPM_CLASSIFY_OPTION0</a> structures.


## -remarks



<b>FWPM_CLASSIFY_OPTIONS0</b> is a specific implementation of FWPM_CLASSIFY_OPTIONS. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550078">FWPM_CLASSIFY_OPTION0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

