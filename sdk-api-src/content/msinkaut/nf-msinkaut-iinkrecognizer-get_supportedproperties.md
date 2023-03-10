---
UID: NF:msinkaut.IInkRecognizer.get_SupportedProperties
title: IInkRecognizer::get_SupportedProperties (msinkaut.h)
description: Gets an array of globally unique identifiers (GUIDs) that describe the properties that the IInkRecognizer object supports.
helpviewer_keywords: ["11153c7f-5284-483b-b1d5-01e670d924b4","IInkRecognizer interface [Tablet PC]","SupportedProperties property","IInkRecognizer.SupportedProperties","IInkRecognizer.get_SupportedProperties","IInkRecognizer::SupportedProperties","IInkRecognizer::get_SupportedProperties","SupportedProperties property [Tablet PC]","SupportedProperties property [Tablet PC]","IInkRecognizer interface","get_SupportedProperties","msinkaut/IInkRecognizer::SupportedProperties","msinkaut/IInkRecognizer::get_SupportedProperties","tablet.iinkrecognizer_supportedproperties"]
old-location: tablet\iinkrecognizer_supportedproperties.htm
tech.root: tablet
ms.assetid: 11153c7f-5284-483b-b1d5-01e670d924b4
ms.date: 12/05/2018
ms.keywords: 11153c7f-5284-483b-b1d5-01e670d924b4, IInkRecognizer interface [Tablet PC],SupportedProperties property, IInkRecognizer.SupportedProperties, IInkRecognizer.get_SupportedProperties, IInkRecognizer::SupportedProperties, IInkRecognizer::get_SupportedProperties, SupportedProperties property [Tablet PC], SupportedProperties property [Tablet PC],IInkRecognizer interface, get_SupportedProperties, msinkaut/IInkRecognizer::SupportedProperties, msinkaut/IInkRecognizer::get_SupportedProperties, tablet.iinkrecognizer_supportedproperties
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkRecognizer::get_SupportedProperties
 - msinkaut/IInkRecognizer::get_SupportedProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognizer.SupportedProperties
 - IInkRecognizer.get_SupportedProperties
 - IInkRecognizer.get_SupportedProperties
---

# IInkRecognizer::get_SupportedProperties


## -description

Gets an array of globally unique identifiers (GUIDs) that describe the properties that the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> object supports.



This property is read-only.

## -parameters

## -remarks

A recognizer may support line metrics, line numbers, confidence levels, and so on. For a complete list of the properties that a recognizer may support, see the <a href="/windows/desktop/tablet/recognitionproperty-constants">RecognitionProperty</a> object.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer Interface</a>



<a href="/windows/desktop/tablet/packetpropertyguids-constants">PacketPropertyGuids Constants</a>