---
UID: NF:ctfspui.ITfSpeechUIServer.UpdateBalloon
title: ITfSpeechUIServer::UpdateBalloon
author: windows-sdk-content
description: ITfSpeechUIServer::UpdateBalloon method
old-location: tsf\itfspeechuiserver_updateballoon.htm
old-project: TSF
ms.assetid: 5ef25aa6-afc4-4c91-8e49-cb5a7ecec36a
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITfSpeechUIServer interface [Text Services Framework],UpdateBalloon method, ITfSpeechUIServer.UpdateBalloon, ITfSpeechUIServer::UpdateBalloon, UpdateBalloon, UpdateBalloon method [Text Services Framework], UpdateBalloon method [Text Services Framework],ITfSpeechUIServer interface, ctfspui/ITfSpeechUIServer::UpdateBalloon, tsf.itfspeechuiserver_updateballoon
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TF_LMLATTELEMENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sptip.dll
api_name:
 - ITfSpeechUIServer.UpdateBalloon
product: Windows
targetos: Windows
req.lib: 
req.dll: Sptip.dll
req.irql: 
---

# ITfSpeechUIServer::UpdateBalloon


## -description




## -parameters




### -param style [in]

Contains a <a href="https://msdn.microsoft.com/c79eb490-b950-4d49-bdf9-821f3706446d">TfLBBalloonStyle</a> element that specifies the balloon style.


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




<a href="https://msdn.microsoft.com/40961001-b659-4ddb-ae7d-5342957770be">ITfSpeechUIServer
      </a>



<a href="https://msdn.microsoft.com/c79eb490-b950-4d49-bdf9-821f3706446d">
        TfLBBalloonStyle
      </a>
 

 

