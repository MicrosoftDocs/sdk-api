---
UID: NF:ctfspui.ITfSpeechUIServer.UpdateBalloon
title: ITfSpeechUIServer::UpdateBalloon (ctfspui.h)
description: ITfSpeechUIServer::UpdateBalloon method
helpviewer_keywords: ["ITfSpeechUIServer interface [Text Services Framework]","UpdateBalloon method","ITfSpeechUIServer.UpdateBalloon","ITfSpeechUIServer::UpdateBalloon","UpdateBalloon","UpdateBalloon method [Text Services Framework]","UpdateBalloon method [Text Services Framework]","ITfSpeechUIServer interface","ctfspui/ITfSpeechUIServer::UpdateBalloon","tsf.itfspeechuiserver_updateballoon"]
old-location: tsf\itfspeechuiserver_updateballoon.htm
tech.root: TSF
ms.assetid: 5ef25aa6-afc4-4c91-8e49-cb5a7ecec36a
ms.date: 12/05/2018
ms.keywords: ITfSpeechUIServer interface [Text Services Framework],UpdateBalloon method, ITfSpeechUIServer.UpdateBalloon, ITfSpeechUIServer::UpdateBalloon, UpdateBalloon, UpdateBalloon method [Text Services Framework], UpdateBalloon method [Text Services Framework],ITfSpeechUIServer interface, ctfspui/ITfSpeechUIServer::UpdateBalloon, tsf.itfspeechuiserver_updateballoon
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
 - ITfSpeechUIServer::UpdateBalloon
 - ctfspui/ITfSpeechUIServer::UpdateBalloon
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
 - ITfSpeechUIServer.UpdateBalloon
---

# ITfSpeechUIServer::UpdateBalloon


## -description

Sets the style and text of the speech balloon on the TSF language bar.

## -parameters

### -param style [in]

Contains a <a href="/windows/win32/api/ctfutb/ne-ctfutb-tflbballoonstyle">TfLBBalloonStyle</a> element that specifies the balloon style.

### -param pch [in]

Pointer to a zero-terminated Unicode string that contains the text to show in the balloon.

### -param cch [in]

Specifies the number of characters in the string of the <i>pch</i> parameter.

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



<a href="/windows/win32/api/ctfutb/ne-ctfutb-tflbballoonstyle">TfLBBalloonStyle
      </a>