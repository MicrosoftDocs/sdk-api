---
UID: NS:winnt._GROUP_RELATIONSHIP
title: "_GROUP_RELATIONSHIP"
author: windows-sdk-content
description: Represents information about processor groups. This structure is used with the GetLogicalProcessorInformationEx function.
old-location: base\group_relationship.htm
tech.root: procthread
ms.assetid: 3529ddef-04c5-4573-877d-c225da684e38
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PGROUP_RELATIONSHIP, GROUP_RELATIONSHIP, GROUP_RELATIONSHIP structure, PGROUP_RELATIONSHIP, PGROUP_RELATIONSHIP structure pointer, _GROUP_RELATIONSHIP, base.group_relationship, winnt/GROUP_RELATIONSHIP, winnt/PGROUP_RELATIONSHIP"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - GROUP_RELATIONSHIP
product: Windows
targetos: Windows
req.typenames: GROUP_RELATIONSHIP, *PGROUP_RELATIONSHIP
req.redist: 
---

# _GROUP_RELATIONSHIP structure


## -description


Represents information about processor groups. This structure is used with the <a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a> function.


## -struct-fields




### -field MaximumGroupCount

The maximum number of processor groups on the system.


### -field ActiveGroupCount

The number of active groups on the system. This member indicates the number of <a href="https://msdn.microsoft.com/6ff9cc3c-34e7-4dc4-94cd-6ed278dfaa03">PROCESSOR_GROUP_INFO</a> structures in the <b>GroupInfo</b> array.


### -field Reserved

This member is reserved.


### -field GroupInfo

An array of <a href="https://msdn.microsoft.com/6ff9cc3c-34e7-4dc4-94cd-6ed278dfaa03">PROCESSOR_GROUP_INFO</a> structures. Each structure represents the number and affinity of processors in an active group on the system.


## -see-also




<a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a>



<a href="https://msdn.microsoft.com/6ff9cc3c-34e7-4dc4-94cd-6ed278dfaa03">PROCESSOR_GROUP_INFO</a>



<a href="https://msdn.microsoft.com/6ff16cda-c1dc-4d5c-ac60-756653cd6b07">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a>
 

 

