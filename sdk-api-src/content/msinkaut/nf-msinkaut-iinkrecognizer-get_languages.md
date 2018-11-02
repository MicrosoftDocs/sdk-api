---
UID: NF:msinkaut.IInkRecognizer.get_Languages
title: IInkRecognizer::get_Languages
author: windows-sdk-content
description: Gets an array of language identifiers for the languages that the IInkRecognizer object supports.
old-location: tablet\iinkrecognizer_languages.htm
tech.root: tablet
ms.assetid: 96419ffa-6af1-4e45-a831-f11564501975
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 96419ffa-6af1-4e45-a831-f11564501975, IInkRecognizer interface [Tablet PC],Languages property, IInkRecognizer.Languages, IInkRecognizer.get_Languages, IInkRecognizer::Languages, IInkRecognizer::get_Languages, Languages property [Tablet PC], Languages property [Tablet PC],IInkRecognizer interface, get_Languages, msinkaut/IInkRecognizer::Languages, msinkaut/IInkRecognizer::get_Languages, tablet.iinkrecognizer_languages
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
 - IInkRecognizer.Languages
 - IInkRecognizer.get_Languages
 - IInkRecognizer.get_Languages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkRecognizer::get_Languages


## -description



Gets an array of language identifiers for the languages that the <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> object supports.



This property is read-only.


## -parameters


## -remarks



This property can be used to search the <a href="https://msdn.microsoft.com/b916e53f-9acd-40dc-961b-ebbecb15bd21">InkRecognizers</a> collection for a <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> that supports a specific language.

This property returns the empty array for Microsoft gesture recognizer.




## -see-also




<a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer Interface</a>



<a href="https://msdn.microsoft.com/701951fd-ffb9-40fd-bb2c-7cdeb330f9b7">Name Property</a>
 

 

