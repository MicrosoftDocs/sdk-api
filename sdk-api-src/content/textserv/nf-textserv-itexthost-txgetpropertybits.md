---
UID: NF:textserv.ITextHost.TxGetPropertyBits
title: ITextHost::TxGetPropertyBits (textserv.h)
description: Requests the bit property settings for the text host.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxGetPropertyBits method","ITextHost.TxGetPropertyBits","ITextHost::TxGetPropertyBits","TxGetPropertyBits","TxGetPropertyBits method [Windows Controls]","TxGetPropertyBits method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxGetPropertyBits","_win32_ITextHost_TxGetPropertyBits_cpp","controls.ITextHost_TxGetPropertyBits","controls._win32_ITextHost_TxGetPropertyBits","textserv/ITextHost::TxGetPropertyBits"]
old-location: controls\ITextHost_TxGetPropertyBits.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxgetpropertybits.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetPropertyBits method, ITextHost.TxGetPropertyBits, ITextHost::TxGetPropertyBits, TxGetPropertyBits, TxGetPropertyBits method [Windows Controls], TxGetPropertyBits method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetPropertyBits, _win32_ITextHost_TxGetPropertyBits_cpp, controls.ITextHost_TxGetPropertyBits, controls._win32_ITextHost_TxGetPropertyBits, textserv/ITextHost::TxGetPropertyBits
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
 - ITextHost::TxGetPropertyBits
 - textserv/ITextHost::TxGetPropertyBits
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
 - ITextHost.TxGetPropertyBits
---

# ITextHost::TxGetPropertyBits


## -description

Requests the bit property settings for the text host.

## -parameters

### -param dwMask [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Mask of properties in which the caller is interested. For the possible bit values, see 
					<i>dwBits</i> in <a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxpropertybitschange">OnTxPropertyBitsChange</a>.

### -param pdwBits [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

The current settings for the properties specified by 
					<i>dwMask</i>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

The return value is <b>S_OK</b>.

## -remarks

This call is valid at any time, for any combination of requested property bits.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>