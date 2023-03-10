---
UID: NF:tom.ITextPara2.SetEffects
title: ITextPara2::SetEffects (tom.h)
description: Sets the paragraph format effects.
helpviewer_keywords: ["ITextPara2 interface [Windows Controls]","SetEffects method","ITextPara2.SetEffects","ITextPara2::SetEffects","SetEffects","SetEffects method [Windows Controls]","SetEffects method [Windows Controls]","ITextPara2 interface","controls.itextpara2_seteffects","tom/ITextPara2::SetEffects"]
old-location: controls\itextpara2_seteffects.htm
tech.root: Controls
ms.assetid: e7184de4-b416-4f28-8f10-c89ffcccf1a1
ms.date: 12/05/2018
ms.keywords: ITextPara2 interface [Windows Controls],SetEffects method, ITextPara2.SetEffects, ITextPara2::SetEffects, SetEffects, SetEffects method [Windows Controls], SetEffects method [Windows Controls],ITextPara2 interface, controls.itextpara2_seteffects, tom/ITextPara2::SetEffects
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
 - ITextPara2::SetEffects
 - tom/ITextPara2::SetEffects
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
 - ITextPara2.SetEffects
---

# ITextPara2::SetEffects


## -description

Sets the paragraph format effects.

## -parameters

### -param Value [in]

Type: <b>long</b>

The paragraph effects value.

This value can be a combination of the flags defined in the table for <a href="/windows/desktop/api/tom/nf-tom-itextpara2-geteffects">ITextPara2::GetEffects</a>.

### -param Mask [in]

Type: <b>long</b>

The desired mask.

This value can be a combination of the flags defined in the table for <a href="/windows/desktop/api/tom/nf-tom-itextpara2-geteffects">ITextPara2::GetEffects</a>. 

Only effects with the corresponding mask flag set are modified.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara2-geteffects">ITextPara2::GetEffects</a>