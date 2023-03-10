---
UID: NF:tom.ITextDocument2.GetStory
title: ITextDocument2::GetStory (tom.h)
description: Retrieves the story that corresponds to a particular index.
helpviewer_keywords: ["GetStory","GetStory method [Windows Controls]","GetStory method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetStory method","ITextDocument2.GetStory","ITextDocument2::GetStory","controls.itextdocument2_getstory","tom/ITextDocument2::GetStory"]
old-location: controls\itextdocument2_getstory.htm
tech.root: Controls
ms.assetid: bb1322e9-47b2-4770-b5de-c5eeda70eed1
ms.date: 12/05/2018
ms.keywords: GetStory, GetStory method [Windows Controls], GetStory method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetStory method, ITextDocument2.GetStory, ITextDocument2::GetStory, controls.itextdocument2_getstory, tom/ITextDocument2::GetStory
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
 - ITextDocument2::GetStory
 - tom/ITextDocument2::GetStory
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
 - ITextDocument2.GetStory
---

# ITextDocument2::GetStory


## -description

Retrieves the story that corresponds to a particular index.

## -parameters

### -param Index [in]

Type: <b>long</b>

The index of the story to retrieve.

### -param ppStory [out, retval]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextstory">ITextStory</a>**</b>

The story.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>