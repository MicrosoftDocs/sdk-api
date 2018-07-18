---
UID: NF:msctf.ITfCompositionSink.OnCompositionTerminated
title: ITfCompositionSink::OnCompositionTerminated
author: windows-sdk-content
description: ITfCompositionSink::OnCompositionTerminated method
old-location: tsf\itfcompositionsink_oncompositionterminated.htm
old-project: TSF
ms.assetid: 4b7c3993-6d01-492f-9bb5-241a1cbd4b63
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfCompositionSink interface [Text Services Framework],OnCompositionTerminated method, ITfCompositionSink.OnCompositionTerminated, ITfCompositionSink::OnCompositionTerminated, OnCompositionTerminated, OnCompositionTerminated method [Text Services Framework], OnCompositionTerminated method [Text Services Framework],ITfCompositionSink interface, _tsf_itfcompositionsink_oncompositionterminated_ref, msctf/ITfCompositionSink::OnCompositionTerminated, tsf.itfcompositionsink_oncompositionterminated
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - imekrcic.dll
api_name:
 - ITfCompositionSink.OnCompositionTerminated
product: Windows
targetos: Windows
req.lib: 
req.dll: Imekrcic.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfCompositionSink::OnCompositionTerminated


## -description




## -parameters




### -param ecWrite [in]

Contains a <a href="https://msdn.microsoft.com/1de17286-5d56-4302-a144-5fe6ca7d5557">TfEditCookie</a> value that identifies the edit context. This is the same value passed for <i>ecWrite</i> in the call to <a href="https://msdn.microsoft.com/aab84e6c-39c7-438e-b4f0-1d174473aa02">ITfContextComposition::StartComposition</a>.


### -param pComposition [in]

Pointer to the <a href="https://msdn.microsoft.com/b1eb5782-13e3-4cbb-8c37-ce7219d1e838">ITfComposition</a> object terminated.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



There is no required action for the TSF text service when this method is called. The TSF text service can use this notification to revert partially composed text into readable text or erase the composition entirely. The TSF manager will automatically clear the GUID_PROP_COMPOSING property value over the affected text.




## -see-also




<a href="https://msdn.microsoft.com/b1eb5782-13e3-4cbb-8c37-ce7219d1e838">
        ITfComposition
      </a>



<a href="https://msdn.microsoft.com/17d5eab5-a308-40a5-823a-f176508dda71">ITfCompositionSink</a>



<a href="https://msdn.microsoft.com/aab84e6c-39c7-438e-b4f0-1d174473aa02">ITfContextComposition::StartComposition
      </a>



<a href="https://msdn.microsoft.com/1de17286-5d56-4302-a144-5fe6ca7d5557">
        TfEditCookie
      </a>
 

 

