---
UID: NS:eaptypes._EAP_TYPE
title: "_EAP_TYPE"
author: windows-driver-content
description: Contains type and vendor identification information for an EAP method.
old-location: eaphost\eap_type.htm
old-project: EAPHost
ms.assetid: 383f1e11-2e40-45e6-8c55-a23d1b8eb71f
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: EAP_TYPE, EAP_TYPE structure [EAPHost], _EAP_TYPE, eaphost.eap_type, eaptypes/EAP_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: eaptypes.h
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
req.typenames: EAP_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	eaptypes.h
api_name:
-	EAP_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _EAP_TYPE structure


## -description


The <b>EAP_TYPE</b> structure contains type and vendor identification information for an EAP method.


## -struct-fields




### -field type

The numeric type code for this EAP method.

<div class="alert"><b>Note</b>  For more information on the allocation of EAP method types, see section 6.2 of <a href="Http://go.microsoft.com/fwlink/p/?linkid=84016">RFC 3748</a>.</div>
<div> </div>

### -field dwVendorId

The vendor ID for the EAP method.


### -field dwVendorType

The numeric type code for the vendor of this EAP method.


## -see-also




<a href="https://msdn.microsoft.com/f6f3b909-1e89-47f8-853c-c0f3f2414817">Common EAPHost API Structures</a>
 

 

