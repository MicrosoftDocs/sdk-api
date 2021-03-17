---
UID: NF:textserv.ITextHost.TxKillTimer
title: ITextHost::TxKillTimer (textserv.h)
description: Requests the text host to destroy the specified timer.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxKillTimer method","ITextHost.TxKillTimer","ITextHost::TxKillTimer","TxKillTimer","TxKillTimer method [Windows Controls]","TxKillTimer method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxKillTimer","_win32_ITextHost_TxKillTimer_cpp","controls.ITextHost_TxKillTimer","controls._win32_ITextHost_TxKillTimer","textserv/ITextHost::TxKillTimer"]
old-location: controls\ITextHost_TxKillTimer.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxkilltimer.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxKillTimer method, ITextHost.TxKillTimer, ITextHost::TxKillTimer, TxKillTimer, TxKillTimer method [Windows Controls], TxKillTimer method [Windows Controls],ITextHost interface, _win32_ITextHost_TxKillTimer, _win32_ITextHost_TxKillTimer_cpp, controls.ITextHost_TxKillTimer, controls._win32_ITextHost_TxKillTimer, textserv/ITextHost::TxKillTimer
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
 - ITextHost::TxKillTimer
 - textserv/ITextHost::TxKillTimer
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
 - ITextHost.TxKillTimer
---

# ITextHost::TxKillTimer


## -description

Requests the text host to destroy the specified timer.

## -parameters

### -param idTimer [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Identifier of the timer created by the <a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txsettimer">ITextHost::TxSetTimer</a> method.

## -remarks

This method may be called at any time, whether the control is active or inactive.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<b>Reference</b>



<a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txsettimer">TxSetTimer</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>