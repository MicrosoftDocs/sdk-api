---
UID: NS:mi._MI_QualifierSet
title: MI_QualifierSet (mi.h)
author: windows-sdk-content
description: Allows the developer to view the qualifiers of a class definition.
old-location: wmi_v2\mi_qualifierset.htm
tech.root: wmi_v2
ms.assetid: 6c374d19-c433-4c70-a644-e53a401f96dd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_QualifierSet, MI_QualifierSet structure [Windows Management Infrastructure (MI)], mi/MI_QualifierSet, wmi_v2.mi_qualifierset
ms.topic: struct
f1_keywords:
- mi/MI_QualifierSet
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
- Mi.h
api_name:
- MI_QualifierSet
product: Windows
targetos: Windows
req.typenames: MI_QualifierSet
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_QualifierSet structure


## -description


Allows the developer to view the qualifiers of a class definition.


## -struct-fields




### -field reserved1

Reserved for internal use.


### -field reserved2

Reserved for internal use.


### -field ft


<a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_qualifiersetft">MI_QualifierSetFT</a> structure holding the function pointers to view the qualifier details. To enumerate over the structure, use the functions containing the "MI_QualifierSet_" prefix.

