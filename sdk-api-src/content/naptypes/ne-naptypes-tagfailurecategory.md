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

# tagFailureCategory enumeration


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>FailureCategory</b> enumeration indicates the source of a failure.


## -enum-fields




### -field failureCategoryNone

No failure.


### -field failureCategoryOther

A failure which is not due to client or server components or communications.


### -field failureCategoryClientComponent

Failure due to client component.


### -field failureCategoryClientCommunication

Failure due to client communication.


### -field failureCategoryServerComponent

Failure due to server component.


### -field failureCategoryServerCommunication

Failure due to server communication.


## -see-also




<a href="https://msdn.microsoft.com/dbf2978f-062a-417b-a6df-a82879e10ec8">FailureCategoryMapping</a>
 

 

