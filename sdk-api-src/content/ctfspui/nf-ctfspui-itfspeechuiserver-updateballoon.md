---
UID: NF:ctfspui.ITfSpeechUIServer.UpdateBalloon
title: ITfSpeechUIServer::UpdateBalloon (ctfspui.h)
author: windows-sdk-content
description: ITfSpeechUIServer::UpdateBalloon method
old-location: tsf\itfspeechuiserver_updateballoon.htm
tech.root: TSF
ms.assetid: 5ef25aa6-afc4-4c91-8e49-cb5a7ecec36a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfSpeechUIServer interface [Text Services Framework],UpdateBalloon method, ITfSpeechUIServer.UpdateBalloon, ITfSpeechUIServer::UpdateBalloon, UpdateBalloon, UpdateBalloon method [Text Services Framework], UpdateBalloon method [Text Services Framework],ITfSpeechUIServer interface, ctfspui/ITfSpeechUIServer::UpdateBalloon, tsf.itfspeechuiserver_updateballoon
ms.topic: method
f1_keywords: 
 - "ctfspui/ITfSpeechUIServer.UpdateBalloon"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sptip.dll
api_name:
 - ITfSpeechUIServer.UpdateBalloon
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfSpeechUIServer::UpdateBalloon


## -description




## -parameters




### -param style [in]

Contains a <a href="https://docs.microsoft.com/windows/win32/api/ctfutb/ne-ctfutb-tflbballoonstyle">TfLBBalloonStyle</a> element that specifies the balloon style.


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




<a href="https://docs.microsoft.com/windows/desktop/api/ctfspui/nn-ctfspui-itfspeechuiserver">ITfSpeechUIServer
      </a>



<a href="https://docs.microsoft.com/windows/win32/api/ctfutb/ne-ctfutb-tflbballoonstyle">TfLBBalloonStyle
      </a>
 

 

