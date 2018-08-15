---
UID: NE:dmoreg.DMO_REGISTER_FLAGS
title: DMO_REGISTER_FLAGS
author: windows-sdk-content
description: The DMO_REGISTER_FLAGS enumeration defines flags that specify registry information for a Microsoft DirectX Media Object (DMO).
old-location: dshow\dmo_register_flags.htm
old-project: DirectShow
ms.assetid: 472be505-a13c-4612-b799-1e9add3ee3fc
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: DMO_REGISTERF_IS_KEYED, DMO_REGISTER_FLAGS, DMO_REGISTER_FLAGS enumeration [DirectShow], DMO_REGISTER_FLAGSEnumeration, dmoreg/DMO_REGISTERF_IS_KEYED, dmoreg/DMO_REGISTER_FLAGS, dshow.dmo_register_flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dmoreg.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dmoreg.h
api_name:
 - DMO_REGISTER_FLAGS
product: Windows
targetos: Windows
req.lib: Dmoguids.lib; Msdmo.lib
req.dll: 
req.irql: 
---

# DMO_REGISTER_FLAGS enumeration


## -description



The <code>DMO_REGISTER_FLAGS</code> enumeration defines flags that specify registry information for a Microsoft DirectX Media Object (DMO).




## -enum-fields




### -field DMO_REGISTERF_IS_KEYED

Use of the DMO is restricted by a software key.


## -remarks



A software key enables the developer of a DMO to control who uses the DMO. If a DMO has a software key, applications must unlock the DMO to use it. The method for unlocking the DMO depends on the implementation. Consult the documentation for the particular DMO.




## -see-also




<a href="https://msdn.microsoft.com/5d60c902-5fb0-419b-b54d-5e3b543c5df8">DMO Enumerated Types</a>



<a href="https://msdn.microsoft.com/4e70569b-8502-4eee-bd23-173269b345d1">DMORegister</a>
 

 

