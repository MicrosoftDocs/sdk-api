---
UID: NF:tom.ITextFont2.GetProperty
title: ITextFont2::GetProperty (tom.h)
description: Gets the value of the specified property. (ITextFont2.GetProperty)
helpviewer_keywords: ["GetProperty","GetProperty method [Windows Controls]","GetProperty method [Windows Controls]","ITextFont2 interface","ITextFont2 interface [Windows Controls]","GetProperty method","ITextFont2.GetProperty","ITextFont2::GetProperty","controls.itextfont2_getproperty","tom/ITextFont2::GetProperty"]
old-location: controls\itextfont2_getproperty.htm
tech.root: Controls
ms.assetid: 1894788a-5612-43a2-af77-131d02fe1261
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [Windows Controls], GetProperty method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetProperty method, ITextFont2.GetProperty, ITextFont2::GetProperty, controls.itextfont2_getproperty, tom/ITextFont2::GetProperty
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
 - ITextFont2::GetProperty
 - tom/ITextFont2::GetProperty
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
 - ITextFont2.GetProperty
---

# ITextFont2::GetProperty


## -description

Gets the value of the specified property.

## -parameters

### -param Type [in]

Type: <b>long</b>

The property ID of the value to return.
See Remarks.

### -param pValue [out]

Type: <b>long*</b>

The property value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Property IDs are defined by the Text Object Model (TOM).  Here are how some of the TOM values are obtained:

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-setproperty">ITextFont2::SetProperty</a>
