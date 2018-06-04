---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# tagDIAGNOSIS_STATUS enumeration


## -description


The <b>DIAGNOSIS_STATUS</b> enumeration describes the result of a hypothesis submitted to a helper class in which the health of a component has been determined.


## -enum-fields




### -field DS_NOT_IMPLEMENTED

A helper class is not implemented


### -field DS_CONFIRMED

The helper class has confirmed a problem existing in its component.


### -field DS_REJECTED

The helper class has determined that no problem exists.


### -field DS_INDETERMINATE

The helper class is unable to determine whether there is a problem.


### -field DS_DEFERRED

The helper class is unable to perform the diagnosis at this time.


### -field DS_PASSTHROUGH

The helper class has identified hypotheses to investigate further, but did not identify any problems in its own component.

Equivalent to <b>DS_INDETERMINATE</b>, but is later updated to <b>DS_REJECTED</b> if no hypothesis is confirmed.

<div class="alert"><b>Note</b>  Available only in Windows 7, Windows Server 2008 R2, and later.</div>
<div> </div>
