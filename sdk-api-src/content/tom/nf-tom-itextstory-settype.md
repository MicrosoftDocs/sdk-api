---
UID: NF:tom.ITextStory.SetType
title: ITextStory::SetType (tom.h)
description: Sets the story type.
helpviewer_keywords: ["ITextStory interface [Windows Controls]","SetType method","ITextStory.SetType","ITextStory::SetType","SetType","SetType method [Windows Controls]","SetType method [Windows Controls]","ITextStory interface","controls.itextstory_settype","tom/ITextStory::SetType"]
old-location: controls\itextstory_settype.htm
tech.root: Controls
ms.assetid: b1fda663-cbfa-4972-bc40-004b82631f92
ms.date: 12/05/2018
ms.keywords: ITextStory interface [Windows Controls],SetType method, ITextStory.SetType, ITextStory::SetType, SetType, SetType method [Windows Controls], SetType method [Windows Controls],ITextStory interface, controls.itextstory_settype, tom/ITextStory::SetType
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
 - ITextStory::SetType
 - tom/ITextStory::SetType
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
 - ITextStory.SetType
---

# ITextStory::SetType


## -description

Sets the story type.

## -parameters

### -param Value [in]

Type: <b>long</b>

The story type. The type values are defined in <a href="/windows/desktop/api/tom/nf-tom-itextstory-gettype">ITextStory::GetType</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstory">ITextStory</a>



<a href="/windows/desktop/api/tom/nf-tom-itextstory-gettype">ITextStory::GetType</a>