---
UID: NF:textserv.ITextHost.TxGetAcceleratorPos
title: ITextHost::TxGetAcceleratorPos (textserv.h)
description: Requests the special character to use for the underlining accelerator character.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxGetAcceleratorPos method","ITextHost.TxGetAcceleratorPos","ITextHost::TxGetAcceleratorPos","TxGetAcceleratorPos","TxGetAcceleratorPos method [Windows Controls]","TxGetAcceleratorPos method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxGetAcceleratorPos","_win32_ITextHost_TxGetAcceleratorPos_cpp","controls.ITextHost_TxGetAcceleratorPos","controls._win32_ITextHost_TxGetAcceleratorPos","textserv/ITextHost::TxGetAcceleratorPos"]
old-location: controls\ITextHost_TxGetAcceleratorPos.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetacceleratorpos.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetAcceleratorPos method, ITextHost.TxGetAcceleratorPos, ITextHost::TxGetAcceleratorPos, TxGetAcceleratorPos, TxGetAcceleratorPos method [Windows Controls], TxGetAcceleratorPos method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetAcceleratorPos, _win32_ITextHost_TxGetAcceleratorPos_cpp, controls.ITextHost_TxGetAcceleratorPos, controls._win32_ITextHost_TxGetAcceleratorPos, textserv/ITextHost::TxGetAcceleratorPos
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
 - ITextHost::TxGetAcceleratorPos
 - textserv/ITextHost::TxGetAcceleratorPos
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
 - ITextHost.TxGetAcceleratorPos
---

# ITextHost::TxGetAcceleratorPos


## -description

Requests the special character to use for the underlining accelerator character.

## -parameters

### -param pcp

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a>*</b>

The character position of the character to underline. This variable is set by the text host. A character position of 
					–1 (that is, negative one) indicates that no character should be underlined.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

The return value is <b>S_OK</b>.

## -remarks

Accelerators allow keyboard shortcuts, or accelerator keys, to various UI elements (such as buttons). Typically, the shortcut character is underlined.

This method tells the text services object which character is the accelerator and thus should be underlined. Note that the text services object does 
				<i>not</i> process accelerators; that is the responsibility of the host.

This method is typically only called if the TXTBIT_SHOWACCELERATOR bit is set in the text services object. See <a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxpropertybitschange">OnTxPropertyBitsChange</a>.

<div class="alert"><b>Note</b>  <i>Any</i> change to the text in the text services object results in the invalidation of the accelerator underlining. In this case, it is the host's responsibility to recalculate the appropriate character position and inform the text services object that a new accelerator is available.</div>
<div> </div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxpropertybitschange">OnTxPropertyBitsChange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>