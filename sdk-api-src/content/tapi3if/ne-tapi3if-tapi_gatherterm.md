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

# TAPI_GATHERTERM enumeration


## -description


The <b>TAPI_GATHERTERM</b> enum is used to describe the reasons why the TAPI Server terminated the gathering of digits on the call.


## -enum-fields




### -field TGT_BUFFERFULL

The requested number of digits has been gathered. The buffer is full.


### -field TGT_TERMDIGIT

One of the termination digits matched a received digit. The matched termination digit is the last digit in the buffer.


### -field TGT_FIRSTTIMEOUT

The first digit timeout expired. The buffer contains no digits.


### -field TGT_INTERTIMEOUT

The interdigit timeout expired. The buffer contains at least one digit.


### -field TGT_CANCEL

The request was canceled by this application, by another application, or because the call terminated.


## -see-also




<a href="https://msdn.microsoft.com/97c123b9-4497-43f3-b747-660d3f9f5848">ITDigitsGatheredEvent::get_GatherTermination</a>
 

 

