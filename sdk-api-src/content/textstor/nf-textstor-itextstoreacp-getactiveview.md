---
UID: NF:textstor.ITextStoreACP.GetActiveView
title: ITextStoreACP::GetActiveView (textstor.h)
description: The ITextStoreACP::GetActiveView method returns a TsViewCookie data type that specifies the current active view.
helpviewer_keywords: ["GetActiveView","GetActiveView method [Text Services Framework]","GetActiveView method [Text Services Framework]","ITextStoreACP interface","ITextStoreACP interface [Text Services Framework]","GetActiveView method","ITextStoreACP.GetActiveView","ITextStoreACP::GetActiveView","_tsf_itextstoreacp_getactiveview_ref","textstor/ITextStoreACP::GetActiveView","tsf.itextstoreacp_getactiveview"]
old-location: tsf\itextstoreacp_getactiveview.htm
tech.root: TSF
ms.assetid: 7739674e-9524-4530-900c-6e7facc3254f
ms.date: 12/05/2018
ms.keywords: GetActiveView, GetActiveView method [Text Services Framework], GetActiveView method [Text Services Framework],ITextStoreACP interface, ITextStoreACP interface [Text Services Framework],GetActiveView method, ITextStoreACP.GetActiveView, ITextStoreACP::GetActiveView, _tsf_itextstoreacp_getactiveview_ref, textstor/ITextStoreACP::GetActiveView, tsf.itextstoreacp_getactiveview
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITextStoreACP::GetActiveView
 - textstor/ITextStoreACP::GetActiveView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACP.GetActiveView
---

# ITextStoreACP::GetActiveView


## -description

The <b>ITextStoreACP::GetActiveView</b> method returns a <a href="/windows/desktop/TSF/tsviewcookie">TsViewCookie</a> data type that specifies the current active view.

## -parameters

### -param pvcView [out]

Receives the <b>TsViewCookie</b> data type that specifies the current active view.

## -returns

This method has no return values.

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a>



<a href="/windows/desktop/TSF/tsviewcookie">TsViewCookie
      </a>