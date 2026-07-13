---
UID: NF:tom.ITextRow.SetProperty
title: ITextRow::SetProperty (tom.h)
description: Sets the value of the specified property. (ITextRow.SetProperty)
helpviewer_keywords: ["ITextRow interface [Windows Controls]","SetProperty method","ITextRow.SetProperty","ITextRow::SetProperty","SetProperty","SetProperty method [Windows Controls]","SetProperty method [Windows Controls]","ITextRow interface","controls.itextrow_setproperty","tom/ITextRow::SetProperty"]
old-location: controls\itextrow_setproperty.htm
tech.root: Controls
ms.assetid: d43172b9-c717-41b2-ba22-aa164a595140
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetProperty method, ITextRow.SetProperty, ITextRow::SetProperty, SetProperty, SetProperty method [Windows Controls], SetProperty method [Windows Controls],ITextRow interface, controls.itextrow_setproperty, tom/ITextRow::SetProperty
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
 - ITextRow::SetProperty
 - tom/ITextRow::SetProperty
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
 - ITextRow.SetProperty
---

# ITextRow::SetProperty


## -description

Sets the value of the specified property.

## -parameters

### -param Type [in]

Type: <b>long</b>

The ID of the  property to set.

### -param Value [in]

Type: <b>long</b>

The value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-getproperty">ITextRow::GetProperty</a>
