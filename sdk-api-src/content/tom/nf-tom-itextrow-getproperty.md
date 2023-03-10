---
UID: NF:tom.ITextRow.GetProperty
title: ITextRow::GetProperty (tom.h)
description: Gets the value of the specified property. (ITextRow.GetProperty)
helpviewer_keywords: ["GetProperty","GetProperty method [Windows Controls]","GetProperty method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetProperty method","ITextRow.GetProperty","ITextRow::GetProperty","controls.itextrow_getproperty","tom/ITextRow::GetProperty"]
old-location: controls\itextrow_getproperty.htm
tech.root: Controls
ms.assetid: ed47033f-14b2-4ca1-89be-f2eab3d148ef
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [Windows Controls], GetProperty method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetProperty method, ITextRow.GetProperty, ITextRow::GetProperty, controls.itextrow_getproperty, tom/ITextRow::GetProperty
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
 - ITextRow::GetProperty
 - tom/ITextRow::GetProperty
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
 - ITextRow.GetProperty
---

# ITextRow::GetProperty


## -description

Gets the value of the specified property.

## -parameters

### -param Type [in]

Type: <b>long</b>

The ID of the property to retrieve.

### -param pValue [out]

Type: <b>long*</b>

The value for the property.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Currently, no extra properties are defined.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setproperty">ITextRow::SetProperty</a>
