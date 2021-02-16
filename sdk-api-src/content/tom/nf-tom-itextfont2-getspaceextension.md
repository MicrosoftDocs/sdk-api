---
UID: NF:tom.ITextFont2.GetSpaceExtension
title: ITextFont2::GetSpaceExtension (tom.h)
description: Gets the East Asian space extension value.
helpviewer_keywords: ["GetSpaceExtension","GetSpaceExtension method [Windows Controls]","GetSpaceExtension method [Windows Controls]","ITextFont2 interface","ITextFont2 interface [Windows Controls]","GetSpaceExtension method","ITextFont2.GetSpaceExtension","ITextFont2::GetSpaceExtension","controls.itextfont2_getspaceextension","tom/ITextFont2::GetSpaceExtension"]
old-location: controls\itextfont2_getspaceextension.htm
tech.root: Controls
ms.assetid: 36623ab5-3584-49c7-aeba-c34cfc8053e6
ms.date: 12/05/2018
ms.keywords: GetSpaceExtension, GetSpaceExtension method [Windows Controls], GetSpaceExtension method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetSpaceExtension method, ITextFont2.GetSpaceExtension, ITextFont2::GetSpaceExtension, controls.itextfont2_getspaceextension, tom/ITextFont2::GetSpaceExtension
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
 - ITextFont2::GetSpaceExtension
 - tom/ITextFont2::GetSpaceExtension
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
 - ITextFont2.GetSpaceExtension
---

# ITextFont2::GetSpaceExtension


## -description

Gets the East Asian space extension value.

## -parameters

### -param pValue [out, retval]

Type: <b>float*</b>

The space extension, in floating-point points.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-setspaceextension">ITextFont2::SetSpaceExtension</a>