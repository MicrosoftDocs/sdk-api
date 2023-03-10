---
UID: NF:textserv.ITextHost.TxReleaseDC
title: ITextHost::TxReleaseDC (textserv.h)
description: Releases the device context obtained by the ITextHost::TxGetDC method.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxReleaseDC method","ITextHost.TxReleaseDC","ITextHost::TxReleaseDC","TxReleaseDC","TxReleaseDC method [Windows Controls]","TxReleaseDC method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxReleaseDC","_win32_ITextHost_TxReleaseDC_cpp","controls.ITextHost_TxReleaseDC","controls._win32_ITextHost_TxReleaseDC","textserv/ITextHost::TxReleaseDC"]
old-location: controls\ITextHost_TxReleaseDC.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxreleasedc.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxReleaseDC method, ITextHost.TxReleaseDC, ITextHost::TxReleaseDC, TxReleaseDC, TxReleaseDC method [Windows Controls], TxReleaseDC method [Windows Controls],ITextHost interface, _win32_ITextHost_TxReleaseDC, _win32_ITextHost_TxReleaseDC_cpp, controls.ITextHost_TxReleaseDC, controls._win32_ITextHost_TxReleaseDC, textserv/ITextHost::TxReleaseDC
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
 - ITextHost::TxReleaseDC
 - textserv/ITextHost::TxReleaseDC
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
 - ITextHost.TxReleaseDC
---

# ITextHost::TxReleaseDC


## -description

Releases the device context obtained by the <a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txgetdc">ITextHost::TxGetDC</a> method.

## -parameters

### -param hdc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

Handle to the device context to release.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Returns 1 if <i>hdc</i> was released; otherwise 0.
                    

For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

## -remarks

This method is only valid when the control is in-place active; calls while the control is inactive may fail.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>