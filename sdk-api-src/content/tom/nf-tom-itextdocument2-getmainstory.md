---
UID: NF:tom.ITextDocument2.GetMainStory
title: ITextDocument2::GetMainStory (tom.h)
description: Gets the main story.
helpviewer_keywords: ["GetMainStory","GetMainStory method [Windows Controls]","GetMainStory method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetMainStory method","ITextDocument2.GetMainStory","ITextDocument2::GetMainStory","controls.itextdocument2_getmainstory","tom/ITextDocument2::GetMainStory"]
old-location: controls\itextdocument2_getmainstory.htm
tech.root: Controls
ms.assetid: 732165f2-e6cd-4f39-85c6-06faebfa65e2
ms.date: 12/05/2018
ms.keywords: GetMainStory, GetMainStory method [Windows Controls], GetMainStory method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetMainStory method, ITextDocument2.GetMainStory, ITextDocument2::GetMainStory, controls.itextdocument2_getmainstory, tom/ITextDocument2::GetMainStory
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
 - ITextDocument2::GetMainStory
 - tom/ITextDocument2::GetMainStory
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
 - ITextDocument2.GetMainStory
---

# ITextDocument2::GetMainStory


## -description

Gets the main story.

## -parameters

### -param ppStory [out, retval]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextstory">ITextStory</a>**</b>

The main story.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A rich edit control automatically includes the main story; a call to the <a href="/windows/desktop/api/tom/nf-tom-itextdocument2-getnewstory">ITextDocument2::GetNewStory</a> method is not required.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>