---
UID: NF:tom.ITextPara2.SetProperty
title: ITextPara2::SetProperty (tom.h)
description: Sets the property value.
helpviewer_keywords: ["ITextPara2 interface [Windows Controls]","SetProperty method","ITextPara2.SetProperty","ITextPara2::SetProperty","SetProperty","SetProperty method [Windows Controls]","SetProperty method [Windows Controls]","ITextPara2 interface","controls.itextpara2_setproperty","tom/ITextPara2::SetProperty"]
old-location: controls\itextpara2_setproperty.htm
tech.root: Controls
ms.assetid: 5a95c055-5118-4c2a-8f63-3a2a3114451e
ms.date: 12/05/2018
ms.keywords: ITextPara2 interface [Windows Controls],SetProperty method, ITextPara2.SetProperty, ITextPara2::SetProperty, SetProperty, SetProperty method [Windows Controls], SetProperty method [Windows Controls],ITextPara2 interface, controls.itextpara2_setproperty, tom/ITextPara2::SetProperty
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
 - ITextPara2::SetProperty
 - tom/ITextPara2::SetProperty
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
 - ITextPara2.SetProperty
---

# ITextPara2::SetProperty


## -description

Sets the property value.

## -parameters

### -param Type [in]

Type: <b>long</b>

The property ID of the property value to set. See <a href="/windows/desktop/api/tom/nf-tom-itextpara2-getproperty">ITextPara2::GetProperty</a> for a list of defined properties.

### -param Value [in]

Type: <b>long</b>

The property value to set.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara2-getproperty">ITextPara2::GetProperty</a>