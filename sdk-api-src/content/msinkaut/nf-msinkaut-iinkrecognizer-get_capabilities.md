---
UID: NF:msinkaut.IInkRecognizer.get_Capabilities
title: IInkRecognizer::get_Capabilities (msinkaut.h)
description: Gets the capabilities of the IInkRecognizer object.
helpviewer_keywords: ["Capabilities property [Tablet PC]","Capabilities property [Tablet PC]","IInkRecognizer interface","IInkRecognizer interface [Tablet PC]","Capabilities property","IInkRecognizer.Capabilities","IInkRecognizer.get_Capabilities","IInkRecognizer::Capabilities","IInkRecognizer::get_Capabilities","c8662817-0a33-4828-8de7-c4ce259738a7","get_Capabilities","msinkaut/IInkRecognizer::Capabilities","msinkaut/IInkRecognizer::get_Capabilities","tablet.iinkrecognizer_capabilities"]
old-location: tablet\iinkrecognizer_capabilities.htm
tech.root: tablet
ms.assetid: c8662817-0a33-4828-8de7-c4ce259738a7
ms.date: 12/05/2018
ms.keywords: Capabilities property [Tablet PC], Capabilities property [Tablet PC],IInkRecognizer interface, IInkRecognizer interface [Tablet PC],Capabilities property, IInkRecognizer.Capabilities, IInkRecognizer.get_Capabilities, IInkRecognizer::Capabilities, IInkRecognizer::get_Capabilities, c8662817-0a33-4828-8de7-c4ce259738a7, get_Capabilities, msinkaut/IInkRecognizer::Capabilities, msinkaut/IInkRecognizer::get_Capabilities, tablet.iinkrecognizer_capabilities
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
 - IInkRecognizer::get_Capabilities
 - msinkaut/IInkRecognizer::get_Capabilities
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
 - IInkRecognizer.Capabilities
 - IInkRecognizer.get_Capabilities
 - IInkRecognizer.get_Capabilities
---

# IInkRecognizer::get_Capabilities


## -description

Gets the capabilities of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> object.



This property is read-only.

## -parameters

## -remarks

A recognizer's capabilities are defined in the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercapabilities">InkRecognizerCapabilities</a> enumeration, and they include whether the recognizer supports character Autocomplete; whether it supports free, lined, or boxed input; and so on. For a complete list of recognizer capabilities, see the <b>InkRecognizerCapabilities</b> enumeration.

To determine if a recognizer has a particular capability, use a bitwise comparison operator to check for that capability.

For information about how to request various recognizer capabilities, or modes, see the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide">Guide</a> property of the <a href="/windows/desktop/tablet/inkrecognizercontext-class">RecognizerContext</a> object.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide">Guide Property</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer Interface</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercapabilities">InkRecognizerCapabilities Enumeration</a>



<a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>