---
UID: NF:msctf.ITfTextInputProcessor.Deactivate
title: ITfTextInputProcessor::Deactivate
author: windows-sdk-content
description: ITfTextInputProcessor::Deactivate method
old-location: tsf\itftextinputprocessor_deactivate.htm
old-project: TSF
ms.assetid: 427190fc-f246-47c6-84e0-a28808a86b6b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Deactivate, Deactivate method [Text Services Framework], Deactivate method [Text Services Framework],ITfTextInputProcessor interface, ITfTextInputProcessor interface [Text Services Framework],Deactivate method, ITfTextInputProcessor.Deactivate, ITfTextInputProcessor::Deactivate, _tsf_itftextinputprocessor_deactivate_ref, msctf/ITfTextInputProcessor::Deactivate, tsf.itftextinputprocessor_deactivate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITfTextInputProcessor.Deactivate
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfTextInputProcessor::Deactivate


## -description




## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



TSF calls this method immediately before releasing its final reference to a text service. This provides the opportunity to perform operations necessary to shut down the text service.

This method usually unadvises sinks for events that involve the text service. It can also close any user interface elements of the text service.

Before this method returns, it must release all references to the <i>ptim</i> parameter passed to the text service by the <a href="https://msdn.microsoft.com/c5fd6b5c-0a78-4b5b-aad5-0c398798cf30">ITfTextInputProcessor::Activate</a> method.




## -see-also




<a href="https://msdn.microsoft.com/d3fd296b-0009-4fc2-bf91-0ad31454f0e8">ITfTextInputProcessor
      </a>



<a href="https://msdn.microsoft.com/c5fd6b5c-0a78-4b5b-aad5-0c398798cf30">ITfTextInputProcessor::Activate
      </a>
 

 

