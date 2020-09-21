---
UID: NF:tom.ITextDocument2.SetActiveStory
title: ITextDocument2::SetActiveStory (tom.h)
description: Sets the active story; that is, the story that receives keyboard and mouse input.
helpviewer_keywords: ["ITextDocument2 interface [Windows Controls]","SetActiveStory method","ITextDocument2.SetActiveStory","ITextDocument2::SetActiveStory","SetActiveStory","SetActiveStory method [Windows Controls]","SetActiveStory method [Windows Controls]","ITextDocument2 interface","controls.itextdocument2_setactivestory","tom/ITextDocument2::SetActiveStory"]
old-location: controls\itextdocument2_setactivestory.htm
tech.root: Controls
ms.assetid: 2c71673c-5119-4906-99e0-1a2aa04589e1
ms.date: 12/05/2018
ms.keywords: ITextDocument2 interface [Windows Controls],SetActiveStory method, ITextDocument2.SetActiveStory, ITextDocument2::SetActiveStory, SetActiveStory, SetActiveStory method [Windows Controls], SetActiveStory method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_setactivestory, tom/ITextDocument2::SetActiveStory
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
 - ITextDocument2::SetActiveStory
 - tom/ITextDocument2::SetActiveStory
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
 - ITextDocument2.SetActiveStory
---

# ITextDocument2::SetActiveStory


## -description

Sets the active story; that is, the story that receives keyboard and mouse input.

## -parameters

### -param pStory [in]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextstory">ITextStory</a>*</b>

The story to set as active.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-getactivestory">ITextDocument2::GetActiveStory</a>