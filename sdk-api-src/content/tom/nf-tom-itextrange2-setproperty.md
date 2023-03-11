---
UID: NF:tom.ITextRange2.SetProperty
title: ITextRange2::SetProperty (tom.h)
description: Sets the value of the specified property. (ITextRange2.SetProperty)
helpviewer_keywords: ["ITextRange2 interface [Windows Controls]","SetProperty method","ITextRange2.SetProperty","ITextRange2::SetProperty","SetProperty","SetProperty method [Windows Controls]","SetProperty method [Windows Controls]","ITextRange2 interface","controls.itextrange2_setproperty","tom/ITextRange2::SetProperty"]
old-location: controls\itextrange2_setproperty.htm
tech.root: Controls
ms.assetid: 0d6c2f44-40e9-48b2-850d-d74d7a50fa0d
ms.date: 12/05/2018
ms.keywords: ITextRange2 interface [Windows Controls],SetProperty method, ITextRange2.SetProperty, ITextRange2::SetProperty, SetProperty, SetProperty method [Windows Controls], SetProperty method [Windows Controls],ITextRange2 interface, controls.itextrange2_setproperty, tom/ITextRange2::SetProperty
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
 - ITextRange2::SetProperty
 - tom/ITextRange2::SetProperty
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
 - ITextRange2.SetProperty
---

# ITextRange2::SetProperty


## -description

Sets the value of the specified property.

## -parameters

### -param Type [in]

Type: <b>long</b>

The ID of the property to set.

### -param Value [in]

Type: <b>long</b>

The new property value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange2-getproperty">ITextRange2::GetProperty</a>
