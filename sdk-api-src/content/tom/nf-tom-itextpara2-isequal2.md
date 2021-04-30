---
UID: NF:tom.ITextPara2.IsEqual2
title: ITextPara2::IsEqual2 (tom.h)
description: Determines whether this text paragraph object has the same properties as the specified text paragraph object.
helpviewer_keywords: ["ITextPara2 interface [Windows Controls]","IsEqual2 method","ITextPara2.IsEqual2","ITextPara2::IsEqual2","IsEqual2","IsEqual2 method [Windows Controls]","IsEqual2 method [Windows Controls]","ITextPara2 interface","controls.itextpara2_isequal2","tom/ITextPara2::IsEqual2"]
old-location: controls\itextpara2_isequal2.htm
tech.root: Controls
ms.assetid: 7817b1bd-6ade-4145-90ff-54561a639dc9
ms.date: 12/05/2018
ms.keywords: ITextPara2 interface [Windows Controls],IsEqual2 method, ITextPara2.IsEqual2, ITextPara2::IsEqual2, IsEqual2, IsEqual2 method [Windows Controls], IsEqual2 method [Windows Controls],ITextPara2 interface, controls.itextpara2_isequal2, tom/ITextPara2::IsEqual2
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
 - ITextPara2::IsEqual2
 - tom/ITextPara2::IsEqual2
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
 - ITextPara2.IsEqual2
---

# ITextPara2::IsEqual2


## -description

Determines whether this text paragraph object has the same properties as the specified text paragraph object.

## -parameters

### -param pPara [in]

Type: <b>ITextPara2*</b>

The text paragraph object to compare against.

### -param pB [out, retval]

Type: <b>long*</b>

A <a href="/windows/desktop/Controls/about-text-object-model">tomBool</a> value that is <b>tomTrue</b> if the text paragraph objects have the same properties, or <b>tomFalse</b> if they don't. This parameter can be <b>NULL</b>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a>