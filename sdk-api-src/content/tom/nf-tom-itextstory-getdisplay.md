---
UID: NF:tom.ITextStory.GetDisplay
title: ITextStory::GetDisplay (tom.h)
description: Gets a new display for a story.
helpviewer_keywords: ["GetDisplay","GetDisplay method [Windows Controls]","GetDisplay method [Windows Controls]","ITextStory interface","ITextStory interface [Windows Controls]","GetDisplay method","ITextStory.GetDisplay","ITextStory::GetDisplay","controls.itextstory_getdisplay","tom/ITextStory::GetDisplay"]
old-location: controls\itextstory_getdisplay.htm
tech.root: Controls
ms.assetid: e9ea7fbc-b814-4dbd-ae8a-9e260b56abab
ms.date: 12/05/2018
ms.keywords: GetDisplay, GetDisplay method [Windows Controls], GetDisplay method [Windows Controls],ITextStory interface, ITextStory interface [Windows Controls],GetDisplay method, ITextStory.GetDisplay, ITextStory::GetDisplay, controls.itextstory_getdisplay, tom/ITextStory::GetDisplay
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tom.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStory::GetDisplay
 - tom/ITextStory::GetDisplay
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tom.h
api_name:
 - ITextStory.GetDisplay
---

# ITextStory::GetDisplay


## -description

Gets a new display for a story.

## -parameters

### -param ppDisplay [out, retval]

Type: <b>IUnknown**</b>

The <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface for a display.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A story can be displayed by calling <a href="/windows/desktop/api/tom/nf-tom-itextstory-setactive">ITextStory::SetActive</a>(<b>tomDisplayActive</b>). The <b>ITextStory::GetDisplay</b> method is included, in case it might be advantageous to have more than one display for a set of <a href="/windows/desktop/api/tom/nn-tom-itextstory">ITextStory</a> interfaces.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstory">ITextStory</a>