---
UID: NF:tom.ITextDocument2.CheckTextLimit
title: ITextDocument2::CheckTextLimit (tom.h)
description: Checks whether the number of characters to be added would exceed the maximum text limit.
helpviewer_keywords: ["CheckTextLimit","CheckTextLimit method [Windows Controls]","CheckTextLimit method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","CheckTextLimit method","ITextDocument2.CheckTextLimit","ITextDocument2::CheckTextLimit","controls.itextdocument2_checktextlimit","tom/ITextDocument2::CheckTextLimit"]
old-location: controls\itextdocument2_checktextlimit.htm
tech.root: Controls
ms.assetid: 2c3aae14-8fa4-47bf-93ae-1d34333f0356
ms.date: 12/05/2018
ms.keywords: CheckTextLimit, CheckTextLimit method [Windows Controls], CheckTextLimit method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],CheckTextLimit method, ITextDocument2.CheckTextLimit, ITextDocument2::CheckTextLimit, controls.itextdocument2_checktextlimit, tom/ITextDocument2::CheckTextLimit
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
 - ITextDocument2::CheckTextLimit
 - tom/ITextDocument2::CheckTextLimit
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
 - ITextDocument2.CheckTextLimit
---

# ITextDocument2::CheckTextLimit


## -description

Checks whether the number of characters to be added would exceed the maximum text limit.

## -parameters

### -param cch [in]

Type: <b>long</b>

The number of characters to be added.

### -param pcch [out]

Type: <b>long*</b>

The number of characters that exceed the maximum text limit. This parameter is 0 if the number of characters does not exceed the limit.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>