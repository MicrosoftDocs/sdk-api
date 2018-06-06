---
UID: NS:mi._MI_QualifierSet
title: "_MI_QualifierSet"
author: windows-sdk-content
description: Allows the developer to view the qualifiers of a class definition.
old-location: wmi_v2\mi_qualifierset.htm
old-project: wmi_v2
ms.assetid: 6c374d19-c433-4c70-a644-e53a401f96dd
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_QualifierSet, MI_QualifierSet structure [Windows Management Infrastructure (MI)], _MI_QualifierSet, mi/MI_QualifierSet, wmi_v2.mi_qualifierset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: MI_QualifierSet
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
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_QualifierSet structure


## -description


Allows the developer to view the qualifiers of a class definition.


## -struct-fields




### -field reserved1

Reserved for internal use.


### -field reserved2

Reserved for internal use.


### -field ft


<a href="https://msdn.microsoft.com/3868c336-e3c1-4977-8c5d-3964c93b6074">MI_QualifierSetFT</a> structure holding the function pointers to view the qualifier details. To enumerate over the structure, use the functions containing the "MI_QualifierSet_" prefix.

