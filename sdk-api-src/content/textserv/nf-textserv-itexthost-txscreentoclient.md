---
UID: NF:textserv.ITextHost.TxScreenToClient
title: ITextHost::TxScreenToClient (textserv.h)
description: Converts the screen coordinates to the text host window coordinates.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxScreenToClient method","ITextHost.TxScreenToClient","ITextHost::TxScreenToClient","TxScreenToClient","TxScreenToClient method [Windows Controls]","TxScreenToClient method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxScreenToClient","_win32_ITextHost_TxScreenToClient_cpp","controls.ITextHost_TxScreenToClient","controls._win32_ITextHost_TxScreenToClient","textserv/ITextHost::TxScreenToClient"]
old-location: controls\ITextHost_TxScreenToClient.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxscreentoclient.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxScreenToClient method, ITextHost.TxScreenToClient, ITextHost::TxScreenToClient, TxScreenToClient, TxScreenToClient method [Windows Controls], TxScreenToClient method [Windows Controls],ITextHost interface, _win32_ITextHost_TxScreenToClient, _win32_ITextHost_TxScreenToClient_cpp, controls.ITextHost_TxScreenToClient, controls._win32_ITextHost_TxScreenToClient, textserv/ITextHost::TxScreenToClient
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
 - ITextHost::TxScreenToClient
 - textserv/ITextHost::TxScreenToClient
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
 - ITextHost.TxScreenToClient
---

# ITextHost::TxScreenToClient


## -description

Converts the screen coordinates to the text host window coordinates.

## -parameters

### -param lppt [in]

Type: <b>LPPOINT</b>

The screen coordinates to convert.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Return <b>TRUE</b> if the call succeeds. 

Return <b>FALSE</b> if the call fails.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>