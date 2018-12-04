---
UID: NE:dmoreg.DMO_ENUM_FLAGS
title: DMO_ENUM_FLAGS
author: windows-sdk-content
description: The DMO_ENUM_FLAGS enumeration defines flags that specify search criteria when enumerating Microsoft DirectX Media Objects (DMOs).
old-location: dshow\dmo_enum_flags.htm
tech.root: DirectShow
ms.assetid: ef2be8d8-99d9-4200-8edb-284a5b216814
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DMO_ENUMF_INCLUDE_KEYED, DMO_ENUM_FLAGS, DMO_ENUM_FLAGS enumeration [DirectShow], DMO_ENUM_FLAGSEnumeration, dmoreg/DMO_ENUMF_INCLUDE_KEYED, dmoreg/DMO_ENUM_FLAGS, dshow.dmo_enum_flags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: dmoreg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - Dmoreg.h
api_name:
 - DMO_ENUM_FLAGS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DMO_ENUM_FLAGS enumeration


## -description



The <code>DMO_ENUM_FLAGS</code> enumeration defines flags that specify search criteria when enumerating Microsoft DirectX Media Objects (DMOs).




## -enum-fields




### -field DMO_ENUMF_INCLUDE_KEYED

The enumeration should include DMOs whose use is restricted by a software key. If this flag is absent, keyed DMOs are omitted from the enumeration.


## -remarks



A software key enables the developer of a DMO to control who uses the DMO. If a DMO has a software key, applications must unlock the DMO to use it. The method for unlocking the DMO depends on the implementation. Consult the documentation for the particular DMO.




## -see-also




<a href="https://msdn.microsoft.com/5d60c902-5fb0-419b-b54d-5e3b543c5df8">DMO Enumerated Types</a>



<a href="https://msdn.microsoft.com/2cb69d28-15be-44fb-a180-98b560848c08">DMOEnum</a>
 

 

