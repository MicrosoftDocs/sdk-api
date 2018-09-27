---
UID: NS:winnt._PROCESSOR_GROUP_INFO
title: "_PROCESSOR_GROUP_INFO"
author: windows-sdk-content
description: Represents the number and affinity of processors in a processor group.
old-location: base\processor_group_info.htm
tech.root: procthread
ms.assetid: 6ff9cc3c-34e7-4dc4-94cd-6ed278dfaa03
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: "*PPROCESSOR_GROUP_INFO, PPROCESSOR_GROUP_INFO, PPROCESSOR_GROUP_INFO structure pointer, PROCESSOR_GROUP_INFO, PROCESSOR_GROUP_INFO structure, _PROCESSOR_GROUP_INFO, base.processor_group_info, winnt/PPROCESSOR_GROUP_INFO, winnt/PROCESSOR_GROUP_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - WinNT.h
api_name:
 - PROCESSOR_GROUP_INFO
product: Windows
targetos: Windows
req.typenames: PROCESSOR_GROUP_INFO, *PPROCESSOR_GROUP_INFO
req.redist: 
---

# _PROCESSOR_GROUP_INFO structure


## -description


Represents the number and affinity of processors in a processor group.


## -struct-fields




### -field MaximumProcessorCount

The maximum number of processors in the group.


### -field ActiveProcessorCount

The number of active processors in the group.


### -field Reserved

This member is reserved.


### -field ActiveProcessorMask

A bitmap that specifies the affinity for zero or more active processors within the group.


## -see-also




<a href="https://msdn.microsoft.com/3529ddef-04c5-4573-877d-c225da684e38">GROUP_RELATIONSHIP</a>
 

 

