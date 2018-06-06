---
UID: NF:msinkaut.IInkRecognitionResult.get_TopAlternate
title: IInkRecognitionResult::get_TopAlternate
author: windows-sdk-content
description: Gets the top alternate of the recognition result.
old-location: tablet\iinkrecognitionresult_topalternate.htm
old-project: tablet
ms.assetid: 6be3d9d1-8c59-48c5-a6a5-10d93b47cd5d
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 6be3d9d1-8c59-48c5-a6a5-10d93b47cd5d, IInkRecognitionResult interface [Tablet PC],TopAlternate property, IInkRecognitionResult.TopAlternate, IInkRecognitionResult.get_TopAlternate, IInkRecognitionResult::TopAlternate, IInkRecognitionResult::get_TopAlternate, TopAlternate property [Tablet PC], TopAlternate property [Tablet PC],IInkRecognitionResult interface, get_TopAlternate, msinkaut/IInkRecognitionResult::TopAlternate, msinkaut/IInkRecognitionResult::get_TopAlternate, tablet.iinkrecognitionresult_topalternate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognitionResult.TopAlternate
 - IInkRecognitionResult.get_TopAlternate
 - IInkRecognitionResult.get_TopAlternate
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkRecognitionResult::get_TopAlternate


## -description



Gets the top alternate of the recognition result.



This property is read-only.


## -parameters


## -remarks



When the recognizer returns a recognition result, the recognition alternates are ranked from the highest confidence level to the lowest confidence level. The recognition alternate with the highest confidence level is selected as the top alternate.

You can use the <a href="https://msdn.microsoft.com/98edc5e9-2388-4f4e-a67f-029ee83be4cb">ModifyTopAlternate</a> method to change which recognition alternate is the top alternate.




## -see-also




<a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate Interface</a>



<a href="https://msdn.microsoft.com/fd7ee250-6f76-419b-8164-0d2717ea288c">IInkRecognitionResult Interface</a>



<a href="https://msdn.microsoft.com/98edc5e9-2388-4f4e-a67f-029ee83be4cb">ModifyTopAlternate Method</a>
 

 

