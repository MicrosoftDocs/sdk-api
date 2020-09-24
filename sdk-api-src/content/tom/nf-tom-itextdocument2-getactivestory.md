---
UID: NF:tom.ITextDocument2.GetActiveStory
title: ITextDocument2::GetActiveStory (tom.h)
description: Gets the active story; that is, the story that receives keyboard and mouse input.
helpviewer_keywords: ["GetActiveStory","GetActiveStory method [Windows Controls]","GetActiveStory method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetActiveStory method","ITextDocument2.GetActiveStory","ITextDocument2::GetActiveStory","controls.itextdocument2_getactivestory","tom/ITextDocument2::GetActiveStory"]
old-location: controls\itextdocument2_getactivestory.htm
tech.root: Controls
ms.assetid: 9849d958-5bcf-44d9-827c-3d5619ba2357
ms.date: 12/05/2018
ms.keywords: GetActiveStory, GetActiveStory method [Windows Controls], GetActiveStory method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetActiveStory method, ITextDocument2.GetActiveStory, ITextDocument2::GetActiveStory, controls.itextdocument2_getactivestory, tom/ITextDocument2::GetActiveStory
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
 - ITextDocument2::GetActiveStory
 - tom/ITextDocument2::GetActiveStory
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
 - ITextDocument2.GetActiveStory
---

# ITextDocument2::GetActiveStory


## -description

Gets the active story; that is, the story that receives keyboard and mouse input.

## -parameters

### -param ppStory [out, retval]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextstory">ITextStory</a>**</b>

The active story.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-setactivestory">ITextDocument2::SetActiveStory</a>