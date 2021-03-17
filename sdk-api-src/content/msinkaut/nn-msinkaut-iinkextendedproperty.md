---
UID: NN:msinkaut.IInkExtendedProperty
title: IInkExtendedProperty (msinkaut.h)
description: Represents the ability to add your own data to a variety of objects within the Tablet PC object model.
helpviewer_keywords: ["53146f37-343a-4886-a0bb-d76d50ca96ba","IInkExtendedProperty","IInkExtendedProperty interface [Tablet PC]","IInkExtendedProperty interface [Tablet PC]","described","msinkaut/IInkExtendedProperty","tablet.iinkextendedproperty"]
old-location: tablet\iinkextendedproperty.htm
tech.root: tablet
ms.assetid: 53146f37-343a-4886-a0bb-d76d50ca96ba
ms.date: 12/05/2018
ms.keywords: 53146f37-343a-4886-a0bb-d76d50ca96ba, IInkExtendedProperty, IInkExtendedProperty interface [Tablet PC], IInkExtendedProperty interface [Tablet PC],described, msinkaut/IInkExtendedProperty, tablet.iinkextendedproperty
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
 - IInkExtendedProperty
 - msinkaut/IInkExtendedProperty
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
 - IInkExtendedProperty
---

# IInkExtendedProperty interface


## -description

Represents the ability to add your own data to a variety of objects within the Tablet PC object model.

## -remarks

Extended properties are application-defined data that can be of whatever form the application requires. The name of the extended property is expressed as a globally unique identifier (GUID).

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties">IInkExtendedProperties Interface</a>