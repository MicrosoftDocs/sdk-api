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

# IInkRecognizer::get_Capabilities


## -description



Gets the capabilities of the <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> object.



This property is read-only.


## -parameters


## -remarks



A recognizer's capabilities are defined in the <a href="https://msdn.microsoft.com/df405aeb-fefd-4bba-9c02-c1865418f76a">InkRecognizerCapabilities</a> enumeration, and they include whether the recognizer supports character Autocomplete; whether it supports free, lined, or boxed input; and so on. For a complete list of recognizer capabilities, see the <b>InkRecognizerCapabilities</b> enumeration.

To determine if a recognizer has a particular capability, use a bitwise comparison operator to check for that capability.

For information about how to request various recognizer capabilities, or modes, see the <a href="https://msdn.microsoft.com/706d28c3-fc5d-496a-a957-daf5ba8d47ca">Guide</a> property of the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">RecognizerContext</a> object.




## -see-also




<a href="https://msdn.microsoft.com/706d28c3-fc5d-496a-a957-daf5ba8d47ca">Guide Property</a>



<a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer Interface</a>



<a href="https://msdn.microsoft.com/df405aeb-fefd-4bba-9c02-c1865418f76a">InkRecognizerCapabilities Enumeration</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>
 

 

