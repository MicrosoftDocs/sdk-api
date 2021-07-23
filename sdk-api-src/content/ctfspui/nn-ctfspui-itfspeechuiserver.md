---
UID: NN:ctfspui.ITfSpeechUIServer
title: ITfSpeechUIServer (ctfspui.h)
description: The ITfSpeechUIServer interface manages the speech-related user interface on the TSF language bar.
helpviewer_keywords: ["ITfSpeechUIServer","ITfSpeechUIServer interface [Text Services Framework]","ITfSpeechUIServer interface [Text Services Framework]","described","ctfspui/ITfSpeechUIServer","tsf.itfspeechuiserver"]
old-location: tsf\itfspeechuiserver.htm
tech.root: TSF
ms.assetid: 40961001-b659-4ddb-ae7d-5342957770be
ms.date: 12/05/2018
ms.keywords: ITfSpeechUIServer, ITfSpeechUIServer interface [Text Services Framework], ITfSpeechUIServer interface [Text Services Framework],described, ctfspui/ITfSpeechUIServer, tsf.itfspeechuiserver
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
 - ITfSpeechUIServer
 - ctfspui/ITfSpeechUIServer
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
 - ITfSpeechUIServer
---

# ITfSpeechUIServer interface


## -description

The <b>ITfSpeechUIServer</b> interface manages the speech-related user interface on the TSF language bar.

## -inheritance

The <b>ITfSpeechUIServer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfSpeechUIServer</b> also has these types of members:

## -remarks

The user interface elements on the TSF language bar managed by this interface include the microphone button, the speech configuration menu button, the dictation button, the command button, and the speech balloon. The standard speech text service usually manages these user interface elements in an application, including initialization. This type of application does not require the <b>ITfSpeechUIServer</b> interface.

An application that does not use the speech text service might require use of the features provided by the speech-related interface elements. In that case, the following code example shows how an application can obtain a pointer to the <b>ITfSpeechUIServer</b> interface by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function with the CLSID_SpeechUIServer <b>CLSID</b>.


```cpp

HRESULT hr;
ITfSpeechUIServer* piSpeechUIServer;

hr = CoCreateInstance(CLSID_SpeechUIServer,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_ITfSpeechUIServer,
                      (void**)&piSpeechUIServer);

```


Subsequently, the application can use the <a href="/windows/desktop/api/ctfspui/nf-ctfspui-itfspeechuiserver-initialize">ITfSpeechUIServer::Initialize</a> method to initialize the user interface and the other methods of the <b>ITfSpeechUIServer</b> interface to manage the user interface.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
