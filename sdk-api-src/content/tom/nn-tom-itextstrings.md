---
UID: NN:tom.ITextStrings
title: ITextStrings (tom.h)
description: The ITextStrings interface represents a collection of rich-text strings that are useful for manipulating rich text.
helpviewer_keywords: ["ITextStrings","ITextStrings interface [Windows Controls]","ITextStrings interface [Windows Controls]","described","controls.itextstrings","tom/ITextStrings"]
old-location: controls\itextstrings.htm
tech.root: Controls
ms.assetid: c878d0db-ac13-4ac9-8601-d1c1ba76cd85
ms.date: 12/05/2018
ms.keywords: ITextStrings, ITextStrings interface [Windows Controls], ITextStrings interface [Windows Controls],described, controls.itextstrings, tom/ITextStrings
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStrings
 - tom/ITextStrings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextStrings
---

# ITextStrings interface


## -description

The <b>ITextStrings</b> interface represents a collection of rich-text strings that are useful for manipulating rich text. In particular, you can use the collection to convert linearly formatted math expressions into built-up form and vice versa. You can also use the collection to collect the concatenation of a set of rich-text strings, or to manipulate a string without changing a primary story. The collection is efficiently implemented by concatenating the strings in a scratch story and maintaining an array of the string counts that identify the strings.

## -inheritance

The <b>ITextStrings</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITextStrings</b> also has these types of members:

