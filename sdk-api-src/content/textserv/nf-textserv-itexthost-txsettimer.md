---
UID: NF:textserv.ITextHost.TxSetTimer
title: ITextHost::TxSetTimer (textserv.h)
description: Requests the text host to create a timer with a specified time-out.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxSetTimer method","ITextHost.TxSetTimer","ITextHost::TxSetTimer","TxSetTimer","TxSetTimer method [Windows Controls]","TxSetTimer method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxSetTimer","_win32_ITextHost_TxSetTimer_cpp","controls.ITextHost_TxSetTimer","controls._win32_ITextHost_TxSetTimer","textserv/ITextHost::TxSetTimer"]
old-location: controls\ITextHost_TxSetTimer.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txsettimer.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxSetTimer method, ITextHost.TxSetTimer, ITextHost::TxSetTimer, TxSetTimer, TxSetTimer method [Windows Controls], TxSetTimer method [Windows Controls],ITextHost interface, _win32_ITextHost_TxSetTimer, _win32_ITextHost_TxSetTimer_cpp, controls.ITextHost_TxSetTimer, controls._win32_ITextHost_TxSetTimer, textserv/ITextHost::TxSetTimer
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
 - ITextHost::TxSetTimer
 - textserv/ITextHost::TxSetTimer
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
 - ITextHost.TxSetTimer
---

# ITextHost::TxSetTimer


## -description

Requests the text host to create a timer with a specified time-out.

## -parameters

### -param idTimer [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Timer identifier.

### -param uTimeout [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Time-out in milliseconds.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Return <b>TRUE</b> if the method succeeds. 

Return <b>FALSE</b> if the method fails.

## -remarks

<i>idTimer</i> is used in <a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txkilltimer">ITextHost::TxKillTimer</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<b>Reference</b>



<a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txkilltimer">TxKillTimer</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>