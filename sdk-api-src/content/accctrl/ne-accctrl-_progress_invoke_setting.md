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

# _PROGRESS_INVOKE_SETTING enumeration


## -description


The <b>PROG_INVOKE_SETTING</b> enumeration indicates the initial setting of the function used to track the progress of a call to the <a href="https://msdn.microsoft.com/caa711c3-301b-4ed7-b1f4-dc6a48563905">TreeSetNamedSecurityInfo</a> or <a href="https://msdn.microsoft.com/adae7d07-a452-409e-b1a1-e9f86f873e39">TreeResetNamedSecurityInfo</a> function.


## -enum-fields




### -field ProgressInvokeNever

Never invoke the progress function.


### -field ProgressInvokeEveryObject

Invoke the progress function for every object.


### -field ProgressInvokeOnError

Invoke the progress function only when an error is encountered.


### -field ProgressCancelOperation

Discontinue the tree operation.

<div class="alert"><b>Note</b>  The original state of the tree will not be reset, and the results are unpredictable.</div>
<div> </div>

### -field ProgressRetryOperation

Retry the tree operation.


### -field ProgressInvokePrePostError

Invoke the progress function before and after applying security on the object and on the error.

