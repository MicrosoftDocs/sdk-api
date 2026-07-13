---
UID: NF:tom.ITextStory.SetProperty
title: ITextStory::SetProperty (tom.h)
description: Sets the value of the specified property. (ITextStory.SetProperty)
helpviewer_keywords: ["ITextStory interface [Windows Controls]","SetProperty method","ITextStory.SetProperty","ITextStory::SetProperty","SetProperty","SetProperty method [Windows Controls]","SetProperty method [Windows Controls]","ITextStory interface","controls.itextstory_setproperty","tom/ITextStory::SetProperty"]
old-location: controls\itextstory_setproperty.htm
tech.root: Controls
ms.assetid: 432afe58-a1ed-45aa-b018-bf608bbb7e2a
ms.date: 12/05/2018
ms.keywords: ITextStory interface [Windows Controls],SetProperty method, ITextStory.SetProperty, ITextStory::SetProperty, SetProperty, SetProperty method [Windows Controls], SetProperty method [Windows Controls],ITextStory interface, controls.itextstory_setproperty, tom/ITextStory::SetProperty
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
 - ITextStory::SetProperty
 - tom/ITextStory::SetProperty
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
 - ITextStory.SetProperty
---

# ITextStory::SetProperty


## -description

Sets the value of the specified property.

## -parameters

### -param Type [in]

Type: <b>long</b>

The Microsoft accountID that identifies the property. Currently, no extra properties are defined.

### -param Value [in]

Type: <b>long</b>

The new property value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstory">ITextStory</a>



<a href="/windows/desktop/api/tom/nf-tom-itextstory-getproperty">ITextStory::GetProperty</a>
