---
UID: NF:msctf.ITfTextInputProcessor.Activate
title: ITfTextInputProcessor::Activate
author: windows-sdk-content
description: ITfTextInputProcessor::Activate method
old-location: tsf\itftextinputprocessor_activate.htm
tech.root: TSF
ms.assetid: c5fd6b5c-0a78-4b5b-aad5-0c398798cf30
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Activate, Activate method [Text Services Framework], Activate method [Text Services Framework],ITfTextInputProcessor interface, ITfTextInputProcessor interface [Text Services Framework],Activate method, ITfTextInputProcessor.Activate, ITfTextInputProcessor::Activate, _tsf_itftextinputprocessor_activate_ref, msctf/ITfTextInputProcessor::Activate, tsf.itftextinputprocessor_activate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
 - ITfTextInputProcessor.Activate
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfTextInputProcessor::Activate


## -description




## -parameters




### -param ptim [in]

Pointer to the <a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr</a> interface for the thread manager that owns the text service.


### -param tid [in]

Specifies the client identifier for the text service.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



TSF calls this method after creating an instance of a text service with a call to <a href="_com_cocreateinstance">CoCreateInstance</a>. This enables operations necessary to start the text service.

This method usually adds a reference to the thread manager for the session and advise sinks for events that involve the text service, such as change of focus, keystrokes, and window events. It also customizes the language bar for the text service.

The corresponding <a href="https://msdn.microsoft.com/427190fc-f246-47c6-84e0-a28808a86b6b">ITfTextInputProcessor::Deactivate</a> method that shuts down the text service must release all references to the <i>ptim</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/d3fd296b-0009-4fc2-bf91-0ad31454f0e8">ITfTextInputProcessor
      </a>



<a href="https://msdn.microsoft.com/427190fc-f246-47c6-84e0-a28808a86b6b">ITfTextInputProcessor::Deactivate
      </a>



<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr
      </a>
 

 

