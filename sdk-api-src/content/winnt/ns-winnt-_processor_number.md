---
UID: NS:winnt._PROCESSOR_NUMBER
title: "_PROCESSOR_NUMBER"
author: windows-sdk-content
description: Represents a logical processor in a processor group.
old-location: base\processor_number.htm
tech.root: ProcThread
ms.assetid: 9005c6d4-07a9-4ce0-9ee2-54880d7244c3
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "*PPROCESSOR_NUMBER, PPROCESSOR_NUMBER, PPROCESSOR_NUMBER structure pointer, PROCESSOR_NUMBER, PROCESSOR_NUMBER structure, _PROCESSOR_NUMBER, base.processor_number, winnt/PPROCESSOR_NUMBER, winnt/PROCESSOR_NUMBER"
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
 - PROCESSOR_NUMBER
product: Windows
targetos: Windows
req.typenames: PROCESSOR_NUMBER, *PPROCESSOR_NUMBER
req.redist: 
---

# _PROCESSOR_NUMBER structure


## -description


Represents a logical processor in a processor group.


## -struct-fields




### -field Group

The processor group to which the logical processor is assigned.


### -field Number

The number of the logical processor relative to the group.


### -field Reserved

This parameter is reserved.


## -see-also




<a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">Processor Groups</a>
 

 

