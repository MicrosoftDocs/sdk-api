---
UID: NF:msinkaut.IInkRecognizer.get_SupportedProperties
title: IInkRecognizer::get_SupportedProperties
author: windows-driver-content
description: Gets an array of globally unique identifiers (GUIDs) that describe the properties that the IInkRecognizer object supports.
old-location: tablet\iinkrecognizer_supportedproperties.htm
old-project: tablet
ms.assetid: 11153c7f-5284-483b-b1d5-01e670d924b4
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 11153c7f-5284-483b-b1d5-01e670d924b4, IInkRecognizer interface [Tablet PC],SupportedProperties property, IInkRecognizer.SupportedProperties, IInkRecognizer.get_SupportedProperties, IInkRecognizer::SupportedProperties, IInkRecognizer::get_SupportedProperties, SupportedProperties property [Tablet PC], SupportedProperties property [Tablet PC],IInkRecognizer interface, get_SupportedProperties, msinkaut/IInkRecognizer::SupportedProperties, msinkaut/IInkRecognizer::get_SupportedProperties, tablet.iinkrecognizer_supportedproperties
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
req.typenames: TabletPropertyMetricUnit
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkRecognizer.SupportedProperties
-	IInkRecognizer.get_SupportedProperties
-	IInkRecognizer.get_SupportedProperties
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IInkRecognizer::get_SupportedProperties


## -description



Gets an array of globally unique identifiers (GUIDs) that describe the properties that the <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> object supports.



This property is read-only.


## -parameters


## -remarks



A recognizer may support line metrics, line numbers, confidence levels, and so on. For a complete list of the properties that a recognizer may support, see the <a href="https://msdn.microsoft.com/2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8">RecognitionProperty</a> object.




## -see-also




<a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer Interface</a>



<a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">PacketPropertyGuids Constants</a>
 

 

