---
UID: NF:textserv.ITextServices.TxGetCachedSize
title: ITextServices::TxGetCachedSize (textserv.h)
description: Returns the cached drawing logical size (if any) that text services is using. Typically, this will be the size of the last client rectangle used in ITextServices::TxDraw, ITextServices::OnTxSetCursor, and so forth, although it is not guaranteed to be.
helpviewer_keywords: ["ITextServices interface [Windows Controls]","TxGetCachedSize method","ITextServices.TxGetCachedSize","ITextServices::TxGetCachedSize","TxGetCachedSize","TxGetCachedSize method [Windows Controls]","TxGetCachedSize method [Windows Controls]","ITextServices interface","_win32_ITextServices_TxGetCachedSize","_win32_ITextServices_TxGetCachedSize_cpp","controls.ITextServices_TxGetCachedSize","controls._win32_ITextServices_TxGetCachedSize","textserv/ITextServices::TxGetCachedSize"]
old-location: controls\ITextServices_TxGetCachedSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetcachedsize.htm
ms.date: 12/05/2018
ms.keywords: ITextServices interface [Windows Controls],TxGetCachedSize method, ITextServices.TxGetCachedSize, ITextServices::TxGetCachedSize, TxGetCachedSize, TxGetCachedSize method [Windows Controls], TxGetCachedSize method [Windows Controls],ITextServices interface, _win32_ITextServices_TxGetCachedSize, _win32_ITextServices_TxGetCachedSize_cpp, controls.ITextServices_TxGetCachedSize, controls._win32_ITextServices_TxGetCachedSize, textserv/ITextServices::TxGetCachedSize
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ITextServices::TxGetCachedSize
 - textserv/ITextServices::TxGetCachedSize
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
 - ITextServices.TxGetCachedSize
---

# ITextServices::TxGetCachedSize


## -description

Returns the cached drawing logical size (if any) that text services is using. Typically, this will be the size of the last client rectangle used in <a href="/windows/desktop/api/textserv/nf-textserv-itextservices-txdraw">ITextServices::TxDraw</a>, <a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxsetcursor">ITextServices::OnTxSetCursor</a>, and so forth, although it is not guaranteed to be.

## -parameters

### -param pdwWidth [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

The width, in client coordinates.

### -param pdwHeight [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

The height (in client coordinates).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, the return value is an <b>HRESULT</b> code.

## -remarks

This method can free the host from the need to maintain the cached drawing size information and the need to keep in synchronization.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a>



<a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxsetcursor">OnTxSetCursor</a>



<b>Reference</b>



<a href="/windows/desktop/api/textserv/nf-textserv-itextservices-txdraw">TxDraw</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>