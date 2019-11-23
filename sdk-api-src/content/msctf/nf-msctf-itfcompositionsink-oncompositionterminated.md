---
UID: NF:msctf.ITfCompositionSink.OnCompositionTerminated
title: ITfCompositionSink::OnCompositionTerminated (msctf.h)

description: ITfCompositionSink::OnCompositionTerminated method
old-location: tsf\itfcompositionsink_oncompositionterminated.htm
tech.root: TSF
ms.assetid: 4b7c3993-6d01-492f-9bb5-241a1cbd4b63

ms.date: 12/05/2018
ms.keywords: ITfCompositionSink interface [Text Services Framework],OnCompositionTerminated method, ITfCompositionSink.OnCompositionTerminated, ITfCompositionSink::OnCompositionTerminated, OnCompositionTerminated, OnCompositionTerminated method [Text Services Framework], OnCompositionTerminated method [Text Services Framework],ITfCompositionSink interface, _tsf_itfcompositionsink_oncompositionterminated_ref, msctf/ITfCompositionSink::OnCompositionTerminated, tsf.itfcompositionsink_oncompositionterminated
ms.topic: method
f1_keywords: 
 - "msctf/ITfCompositionSink.OnCompositionTerminated"
dev_langs:
 - c++
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
req.lib: 
req.dll: Imekrcic.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imekrcic.dll
api_name:
 - ITfCompositionSink.OnCompositionTerminated
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfCompositionSink::OnCompositionTerminated


## -description




## -parameters




### -param ecWrite [in]

Contains a <a href="https://docs.microsoft.com/windows/desktop/TSF/tfeditcookie">TfEditCookie</a> value that identifies the edit context. This is the same value passed for <i>ecWrite</i> in the call to <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextcomposition-startcomposition">ITfContextComposition::StartComposition</a>.


### -param pComposition [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcomposition">ITfComposition</a> object terminated.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



There is no required action for the TSF text service when this method is called. The TSF text service can use this notification to revert partially composed text into readable text or erase the composition entirely. The TSF manager will automatically clear the GUID_PROP_COMPOSING property value over the affected text.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcomposition">ITfComposition
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcompositionsink">ITfCompositionSink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextcomposition-startcomposition">ITfContextComposition::StartComposition
      </a>



<a href="https://docs.microsoft.com/windows/desktop/TSF/tfeditcookie">TfEditCookie
      </a>
 

 

