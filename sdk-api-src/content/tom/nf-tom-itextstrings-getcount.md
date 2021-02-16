---
UID: NF:tom.ITextStrings.GetCount
title: ITextStrings::GetCount (tom.h)
description: Gets the number of strings in a string collection.
helpviewer_keywords: ["GetCount","GetCount method [Windows Controls]","GetCount method [Windows Controls]","ITextStrings interface","ITextStrings interface [Windows Controls]","GetCount method","ITextStrings.GetCount","ITextStrings::GetCount","controls.itextstrings_getcount","tom/ITextStrings::GetCount"]
old-location: controls\itextstrings_getcount.htm
tech.root: Controls
ms.assetid: 6bbe53ab-bd03-4445-8d36-0186a43da451
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [Windows Controls], GetCount method [Windows Controls],ITextStrings interface, ITextStrings interface [Windows Controls],GetCount method, ITextStrings.GetCount, ITextStrings::GetCount, controls.itextstrings_getcount, tom/ITextStrings::GetCount
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
 - ITextStrings::GetCount
 - tom/ITextStrings::GetCount
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
 - ITextStrings.GetCount
---

# ITextStrings::GetCount


## -description

Gets the number of strings in a string collection.

## -parameters

### -param pCount [out, retval]

Type: <b>long*</b>

The count of strings.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstrings">ITextStrings</a>