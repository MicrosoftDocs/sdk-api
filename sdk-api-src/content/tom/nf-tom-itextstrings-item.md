---
UID: NF:tom.ITextStrings.Item
title: ITextStrings::Item (tom.h)
description: Gets an ITextRange2 object for a selected index in a string collection.
helpviewer_keywords: ["ITextStrings interface [Windows Controls]","Item method","ITextStrings.Item","ITextStrings::Item","Item","Item method [Windows Controls]","Item method [Windows Controls]","ITextStrings interface","controls.itextstrings_item","tom/ITextStrings::Item"]
old-location: controls\itextstrings_item.htm
tech.root: Controls
ms.assetid: 8eed4bc6-75a8-440e-a334-543e7b996df0
ms.date: 12/05/2018
ms.keywords: ITextStrings interface [Windows Controls],Item method, ITextStrings.Item, ITextStrings::Item, Item, Item method [Windows Controls], Item method [Windows Controls],ITextStrings interface, controls.itextstrings_item, tom/ITextStrings::Item
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
 - ITextStrings::Item
 - tom/ITextStrings::Item
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
 - ITextStrings.Item
---

# ITextStrings::Item


## -description

Gets an <a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a> object for a selected index in a string collection.

## -parameters

### -param Index [in]

Type: <b>long</b>

The index of the string to retrieve. The default value is 1.

### -param ppRange [out, retval]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>**</b>

The object to receive the range.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The first string corresponds to Index = 1 and the last to Count which is given by <a href="/windows/desktop/api/tom/nf-tom-itextstrings-getcount">ITextStrings_GetCount</a>.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstrings">ITextStrings</a>