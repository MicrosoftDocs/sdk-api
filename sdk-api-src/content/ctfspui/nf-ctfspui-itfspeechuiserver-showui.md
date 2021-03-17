---
UID: NF:ctfspui.ITfSpeechUIServer.ShowUI
title: ITfSpeechUIServer::ShowUI (ctfspui.h)
description: ITfSpeechUIServer::ShowUI method
helpviewer_keywords: ["ITfSpeechUIServer interface [Text Services Framework]","ShowUI method","ITfSpeechUIServer.ShowUI","ITfSpeechUIServer::ShowUI","ShowUI","ShowUI method [Text Services Framework]","ShowUI method [Text Services Framework]","ITfSpeechUIServer interface","ctfspui/ITfSpeechUIServer::ShowUI","tsf.itfspeechuiserver_showui"]
old-location: tsf\itfspeechuiserver_showui.htm
tech.root: TSF
ms.assetid: 4491a3f0-b748-45a8-a8bd-c8fa78d49fa7
ms.date: 12/05/2018
ms.keywords: ITfSpeechUIServer interface [Text Services Framework],ShowUI method, ITfSpeechUIServer.ShowUI, ITfSpeechUIServer::ShowUI, ShowUI, ShowUI method [Text Services Framework], ShowUI method [Text Services Framework],ITfSpeechUIServer interface, ctfspui/ITfSpeechUIServer::ShowUI, tsf.itfspeechuiserver_showui
req.header: ctfspui.h
req.include-header: Ctfutb.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Sptip.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfSpeechUIServer::ShowUI
 - ctfspui/ITfSpeechUIServer::ShowUI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sptip.dll
api_name:
 - ITfSpeechUIServer.ShowUI
---

# ITfSpeechUIServer::ShowUI


## -description

Sets the visibility state of the speech-related user interface elements on the TSF language bar.

## -parameters

### -param fShow [in]

Specifies whether to show (TRUE) or not show (FALSE) the speech-related user interface elements.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctfspui/nn-ctfspui-itfspeechuiserver">ITfSpeechUIServer
      </a>