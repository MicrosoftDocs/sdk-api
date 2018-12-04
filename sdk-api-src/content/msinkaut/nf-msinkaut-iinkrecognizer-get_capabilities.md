---
UID: NF:msinkaut.IInkRecognizer.get_Capabilities
title: IInkRecognizer::get_Capabilities
author: windows-sdk-content
description: Gets the capabilities of the IInkRecognizer object.
old-location: tablet\iinkrecognizer_capabilities.htm
tech.root: tablet
ms.assetid: c8662817-0a33-4828-8de7-c4ce259738a7
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: Capabilities property [Tablet PC], Capabilities property [Tablet PC],IInkRecognizer interface, IInkRecognizer interface [Tablet PC],Capabilities property, IInkRecognizer.Capabilities, IInkRecognizer.get_Capabilities, IInkRecognizer::Capabilities, IInkRecognizer::get_Capabilities, c8662817-0a33-4828-8de7-c4ce259738a7, get_Capabilities, msinkaut/IInkRecognizer::Capabilities, msinkaut/IInkRecognizer::get_Capabilities, tablet.iinkrecognizer_capabilities
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognizer.Capabilities
 - IInkRecognizer.get_Capabilities
 - IInkRecognizer.get_Capabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

