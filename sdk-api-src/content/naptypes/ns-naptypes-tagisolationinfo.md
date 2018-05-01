---
UID: NS:naptypes.tagIsolationInfo
title: tagIsolationInfo
author: windows-driver-content
description: Defines the isolation status of the machine or the connection.
old-location: nap\isolationinfo_struct.htm
old-project: NAP
ms.assetid: ab5e54ab-de5d-489d-bff7-3be4f3973e7a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IsolationInfo, IsolationInfo structure [NAP], nap.isolationinfo_struct, naptypes/IsolationInfo, tagIsolationInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IsolationInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	NapTypes.h
api_name:
-	IsolationInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# tagIsolationInfo structure


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>IsolationInfo</b> structure defines the isolation status of the machine or the connection.


## -struct-fields




### -field isolationState

An <a href="https://msdn.microsoft.com/79f81e8e-a105-4cc9-b175-8a364648f3a6">IsolationState</a> values that contains the isolation state of a machine.


### -field probEndTime

A <a href="https://msdn.microsoft.com/54f2866b-4333-4fc8-bb25-b7d4ae72b7dc">ProbationTime</a> value that contains the time at which a machine should come out from probation.


### -field failureUrl

A <a href="https://msdn.microsoft.com/92261dd3-504d-4a4b-b6fa-86f4f97a0df0">CountedString</a> value that contains a URL to navigate to in the event of failure.


## -see-also




<a href="https://msdn.microsoft.com/92261dd3-504d-4a4b-b6fa-86f4f97a0df0">CountedString</a>



<a href="https://msdn.microsoft.com/79f81e8e-a105-4cc9-b175-8a364648f3a6">IsolationState</a>



<a href="https://msdn.microsoft.com/e391be3c-95ab-4c80-a5d8-8a8fef28e56b">NAP Reference</a>



<a href="https://msdn.microsoft.com/68048587-0f7e-48d4-9326-768a977ea3ee">NAP Structures</a>
 

 

