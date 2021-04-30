---
UID: NF:tom.ITextDocument2.GetDisplays
title: ITextDocument2::GetDisplays (tom.h)
description: Gets the displays collection for this Text Object Model (TOM) engine instance.
helpviewer_keywords: ["GetDisplays","GetDisplays method [Windows Controls]","GetDisplays method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetDisplays method","ITextDocument2.GetDisplays","ITextDocument2::GetDisplays","controls.itextdocument2_getdisplays","tom/ITextDocument2::GetDisplays"]
old-location: controls\itextdocument2_getdisplays.htm
tech.root: Controls
ms.assetid: 8f610b45-9c17-4b20-82e0-fa78169360cc
ms.date: 12/05/2018
ms.keywords: GetDisplays, GetDisplays method [Windows Controls], GetDisplays method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetDisplays method, ITextDocument2.GetDisplays, ITextDocument2::GetDisplays, controls.itextdocument2_getdisplays, tom/ITextDocument2::GetDisplays
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
 - ITextDocument2::GetDisplays
 - tom/ITextDocument2::GetDisplays
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
 - ITextDocument2.GetDisplays
---

# ITextDocument2::GetDisplays


## -description

Gets the displays collection for this Text Object Model (TOM) engine instance.

## -parameters

### -param ppDisplays [out, retval]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextdisplays">ITextDisplays</a>**</b>

The displays collection.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The rich edit control doesn't implement this method.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>