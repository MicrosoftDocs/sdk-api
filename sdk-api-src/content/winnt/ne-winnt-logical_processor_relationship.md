---
UID: NE:winnt._LOGICAL_PROCESSOR_RELATIONSHIP
title: LOGICAL_PROCESSOR_RELATIONSHIP
author: windows-sdk-content
description: Represents the relationship between the processor set identified in the corresponding SYSTEM_LOGICAL_PROCESSOR_INFORMATION or SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX structure.
old-location: base\logical_processor_relationship.htm
tech.root: ProcThread
ms.assetid: 2ada52f0-70ec-4146-9ef7-9af3b08996f9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: LOGICAL_PROCESSOR_RELATIONSHIP, LOGICAL_PROCESSOR_RELATIONSHIP enumeration, RelationAll, RelationCache, RelationGroup, RelationNumaNode, RelationProcessorCore, RelationProcessorPackage, base.logical_processor_relationship, winnt/LOGICAL_PROCESSOR_RELATIONSHIP, winnt/RelationAll, winnt/RelationCache, winnt/RelationGroup, winnt/RelationNumaNode, winnt/RelationProcessorCore, winnt/RelationProcessorPackage
ms.topic: enum
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - LOGICAL_PROCESSOR_RELATIONSHIP
product: Windows
targetos: Windows
req.typenames: LOGICAL_PROCESSOR_RELATIONSHIP
req.redist: 
---

# LOGICAL_PROCESSOR_RELATIONSHIP enumeration


## -description


Represents the relationship between the processor set identified in the corresponding <a href="https://msdn.microsoft.com/32ef5dd8-c00d-44ee-a291-a18653beb1b9">SYSTEM_LOGICAL_PROCESSOR_INFORMATION</a>  or <a href="https://msdn.microsoft.com/en-us/library/Dd405522(v=VS.85).aspx">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a>  structure.


## -enum-fields




### -field RelationProcessorCore

The specified logical processors share a single processor core.


### -field RelationNumaNode

The specified logical processors  are part of the same NUMA node.


### -field RelationCache

The specified logical processors  share a cache. 

<b>Windows Server 2003:  </b>This value is not supported until Windows Server 2003 with SP1 and Windows XP Professional x64 Edition.


### -field RelationProcessorPackage

The specified logical processors share a physical package (a single package socketed or soldered onto a motherboard may contain multiple processor cores or threads, each of which is treated as a separate processor by the operating system).

<b>Windows Server 2003:  </b>This value is not supported until Windows Server 2003 with SP1 and Windows XP Professional x64 Edition.


### -field RelationGroup

The specified logical processors share a single <a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">processor group</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP Professional x64 Edition:  </b>This value is not supported until Windows Server 2008 R2.


### -field RelationAll

On input, retrieves information about all possible relationship types. This value is not used on output.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP Professional x64 Edition:  </b>This value is not supported  until Windows Server 2008 R2.


## -remarks



The value specified by this enumeration indicates the relationship represented in the corresponding <a href="https://msdn.microsoft.com/32ef5dd8-c00d-44ee-a291-a18653beb1b9">SYSTEM_LOGICAL _PROCESSOR_INFORMATION</a>  or <a href="https://msdn.microsoft.com/en-us/library/Dd405522(v=VS.85).aspx">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a>  structure. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/904d2d35-f419-4e8f-a689-f39ed926644c">GetLogicalProcessorInformation</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/904d2d35-f419-4e8f-a689-f39ed926644c">GetLogicalProcessorInformation</a>



<a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a>



<a href="https://msdn.microsoft.com/32ef5dd8-c00d-44ee-a291-a18653beb1b9">SYSTEM_LOGICAL_PROCESSOR_INFORMATION</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd405522(v=VS.85).aspx">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a>
 

 

