---
UID: NF:tom.ITextStory.SetActive
title: ITextStory::SetActive (tom.h)
description: Sets the active state of a story. (ITextStory.SetActive)
helpviewer_keywords: ["ITextStory interface [Windows Controls]","SetActive method","ITextStory.SetActive","ITextStory::SetActive","SetActive","SetActive method [Windows Controls]","SetActive method [Windows Controls]","ITextStory interface","controls.itextstory_setactive","tom/ITextStory::SetActive"]
old-location: controls\itextstory_setactive.htm
tech.root: Controls
ms.assetid: fa0177be-2016-4205-b121-921dbdbf5b71
ms.date: 12/05/2018
ms.keywords: ITextStory interface [Windows Controls],SetActive method, ITextStory.SetActive, ITextStory::SetActive, SetActive, SetActive method [Windows Controls], SetActive method [Windows Controls],ITextStory interface, controls.itextstory_setactive, tom/ITextStory::SetActive
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
 - ITextStory::SetActive
 - tom/ITextStory::SetActive
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
 - ITextStory.SetActive
---

# ITextStory::SetActive


## -description

Sets the active state of a story.

## -parameters

### -param Value [in]

Type: <b>long</b>

The active state. For values, see the <a href="/windows/desktop/api/tom/nf-tom-itextstory-getactive">ITextStory::GetActive</a> method.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstory">ITextStory</a>



<a href="/windows/desktop/api/tom/nf-tom-itextstory-getactive">ITextStory::GetActive</a>
