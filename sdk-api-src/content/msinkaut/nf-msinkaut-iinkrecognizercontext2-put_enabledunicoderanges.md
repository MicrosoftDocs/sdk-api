---
UID: NF:msinkaut.IInkRecognizerContext2.put_EnabledUnicodeRanges
title: IInkRecognizerContext2::put_EnabledUnicodeRanges
author: windows-sdk-content
description: Gets or sets a set of one or more Unicode ranges that the recognizer context will support.
old-location: tablet\iinkrecognizercontext2_enabledunicoderanges.htm
tech.root: tablet
ms.assetid: d976eed0-32d0-47ab-931e-177635f95875
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: EnabledUnicodeRanges property [Tablet PC], EnabledUnicodeRanges property [Tablet PC],IInkRecognizerContext2 interface, IInkRecognizerContext2 interface [Tablet PC],EnabledUnicodeRanges property, IInkRecognizerContext2.EnabledUnicodeRanges, IInkRecognizerContext2.get_EnabledUnicodeRanges, IInkRecognizerContext2.put_EnabledUnicodeRanges, IInkRecognizerContext2::EnabledUnicodeRanges, IInkRecognizerContext2::get_EnabledUnicodeRanges, IInkRecognizerContext2::put_EnabledUnicodeRanges, msinkaut/IInkRecognizerContext2::EnabledUnicodeRanges, msinkaut/IInkRecognizerContext2::get_EnabledUnicodeRanges, msinkaut/IInkRecognizerContext2::put_EnabledUnicodeRanges, put_EnabledUnicodeRanges, tablet.iinkrecognizercontext2_enabledunicoderanges
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
 - IInkRecognizerContext2.EnabledUnicodeRanges
 - IInkRecognizerContext2.get_EnabledUnicodeRanges
 - IInkRecognizerContext2.put_EnabledUnicodeRanges
 - IInkRecognizerContext2.get_EnabledUnicodeRanges
 - IInkRecognizerContext2.put_EnabledUnicodeRanges
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkRecognizerContext2::put_EnabledUnicodeRanges


## -description


Gets or sets a set of one or more Unicode ranges that the recognizer context will support.

This property is read/write.


## -parameters


## -remarks



Use this method to specify a sub-set of Unicode character ranges that the recognizer should use during recognition. This is particularly useful when working with Asian character set where only a sub-set of the characters are commonly used.

Your application should check whether all input ranges are supported by the recognizer. TPC_S_TRUNCATED is returned to indicate that the Unicode ranges passed in were accepted, with the exception of those which were not valid. You can call <b>get_EnabledUnicodeRanges</b> to determine the ranges that were accepted. 




## -see-also




<a href="https://msdn.microsoft.com/ee24c95e-54b1-45a7-a077-4e418d83b1d5">IInkRecognizerContext2 Interface</a>
 

 

