---
UID: NN:ctfspui.ITfSpeechUIServer
title: ITfSpeechUIServer
author: windows-sdk-content
description: The ITfSpeechUIServer interface manages the speech-related user interface on the TSF language bar.
old-location: tsf\itfspeechuiserver.htm
old-project: TSF
ms.assetid: 40961001-b659-4ddb-ae7d-5342957770be
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfSpeechUIServer, ITfSpeechUIServer interface [Text Services Framework], ITfSpeechUIServer interface [Text Services Framework],described, ctfspui/ITfSpeechUIServer, tsf.itfspeechuiserver
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ITfSpeechUIServer
product: Windows
targetos: Windows
req.lib: 
req.dll: Sptip.dll
req.irql: 
---

# ITfSpeechUIServer interface


## -description


The <b>ITfSpeechUIServer</b> interface manages the speech-related user interface on the TSF language bar.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfSpeechUIServer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfSpeechUIServer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfSpeechUIServer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the speech-related user interface elements on the TSF language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4491a3f0-b748-45a8-a8bd-c8fa78d49fa7">ShowUI</a>
</td>
<td align="left" width="63%">
Sets the visibility state of the speech-related user interface elements on the TSF language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ef25aa6-afc4-4c91-8e49-cb5a7ecec36a">UpdateBalloon</a>
</td>
<td align="left" width="63%">
Sets the style and text of the speech balloon on the TSF language bar.

</td>
</tr>
</table> 


## -remarks



The user interface elements on the TSF language bar managed by this interface include the microphone button, the speech configuration menu button, the dictation button, the command button, and the speech balloon. The standard speech text service usually manages these user interface elements in an application, including initialization. This type of application does not require the <b>ITfSpeechUIServer</b> interface.

An application that does not use the speech text service might require use of the features provided by the speech-related interface elements. In that case, the following code example shows how an application can obtain a pointer to the <b>ITfSpeechUIServer</b> interface by calling the <a href="https://msdn.microsoft.com/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function with the CLSID_SpeechUIServer <b>CLSID</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT hr;
ITfSpeechUIServer* piSpeechUIServer;

hr = CoCreateInstance(CLSID_SpeechUIServer,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_ITfSpeechUIServer,
                      (void**)&amp;piSpeechUIServer);
</pre>
</td>
</tr>
</table></span></div>
Subsequently, the application can use the <a href="https://msdn.microsoft.com/5a51b8c7-3d29-4566-8cfa-f76dfd067aa8">ITfSpeechUIServer::Initialize</a> method to initialize the user interface and the other methods of the <b>ITfSpeechUIServer</b> interface to manage the user interface.




## -see-also




<a href="https://msdn.microsoft.com/library/ms686615(v=VS.85).aspx">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

