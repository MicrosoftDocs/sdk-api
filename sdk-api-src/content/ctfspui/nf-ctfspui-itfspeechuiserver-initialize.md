---
UID: NF:ctfspui.ITfSpeechUIServer.Initialize
title: ITfSpeechUIServer::Initialize (ctfspui.h)
description: ITfSpeechUIServer::Initialize method
helpviewer_keywords: ["ITfSpeechUIServer interface [Text Services Framework]","Initialize method","ITfSpeechUIServer.Initialize","ITfSpeechUIServer::Initialize","Initialize","Initialize method [Text Services Framework]","Initialize method [Text Services Framework]","ITfSpeechUIServer interface","ctfspui/ITfSpeechUIServer::Initialize","tsf.itfspeechuiserver_initialize"]
old-location: tsf\itfspeechuiserver_initialize.htm
tech.root: TSF
ms.assetid: 5a51b8c7-3d29-4566-8cfa-f76dfd067aa8
ms.date: 12/05/2018
ms.keywords: ITfSpeechUIServer interface [Text Services Framework],Initialize method, ITfSpeechUIServer.Initialize, ITfSpeechUIServer::Initialize, Initialize, Initialize method [Text Services Framework], Initialize method [Text Services Framework],ITfSpeechUIServer interface, ctfspui/ITfSpeechUIServer::Initialize, tsf.itfspeechuiserver_initialize
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
 - ITfSpeechUIServer::Initialize
 - ctfspui/ITfSpeechUIServer::Initialize
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
 - ITfSpeechUIServer.Initialize
---

# ITfSpeechUIServer::Initialize


## -description

Initializes the speech-related user interface elements on the TSF language bar.



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

## -remarks

The standard speech text service usually initializes the speech-related user interface on the TSF language bar. When a TSF-enabled application, that does not use the speech text service, requires use of the <a href="/windows/desktop/api/ctfspui/nn-ctfspui-itfspeechuiserver">ITfSpeechUIServer</a> interface, it initializes the user interface with this method.

## -see-also

<a href="/windows/desktop/api/ctfspui/nn-ctfspui-itfspeechuiserver">ITfSpeechUIServer
      </a>
