---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0007
title: "__MIDL___MIDL_itf_pla_0001_0043_0007"
author: windows-sdk-content
description: Defines the action to take when committing changes to the data collector set.
old-location: pla\commitmode.htm
old-project: PLA
ms.assetid: 3c485b4d-ba0b-456a-b942-27829371d7fb
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: CommitMode, CommitMode enumeration [PLA], __MIDL___MIDL_itf_pla_0001_0043_0007, base.commitmode, pla.commitmode, pla/CommitMode, pla/plaCreateNew, pla/plaCreateOrModify, pla/plaFlushTrace, pla/plaModify, pla/plaUpdateRunningInstance, pla/plaValidateOnly, plaCreateNew, plaCreateOrModify, plaFlushTrace, plaModify, plaUpdateRunningInstance, plaValidateOnly
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: pla.h
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
req.typenames: CommitMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Pla.h
api_name:
-	CommitMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __MIDL___MIDL_itf_pla_0001_0043_0007 enumeration


## -description


Defines the action to take when committing changes to the data collector set.


## -enum-fields




### -field plaCreateNew

Save the set. The set must not already exist. 

The set is not saved if it is a trace session.


### -field plaModify

Update a previously saved set.


### -field plaCreateOrModify

Save the set. If the set already exists, update the set.

The set is not saved if it is a trace session.


### -field plaUpdateRunningInstance

Apply the updated property values to the currently running data set.


### -field plaFlushTrace

Flush the buffers for an Event Tracing for Windows trace session. This action applies only to sets that contain trace data collectors.


### -field plaValidateOnly

Perform validation only on the set.


## -remarks



All commit modes validate the set.




## -see-also




<a href="https://msdn.microsoft.com/7e432e1f-4b86-45dc-93d5-df603068273d">IDataCollectorSet::Commit</a>
 

 

