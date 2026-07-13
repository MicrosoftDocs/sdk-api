---
UID: NN:ctffunc.ITfFnShowHelp
title: ITfFnShowHelp (ctffunc.h)
description: The ITfFnShowHelp interface is implemented by a text service to enable the language bar to place a help command for the text service in the language bar help menu.
helpviewer_keywords: ["ITfFnShowHelp","ITfFnShowHelp interface [Text Services Framework]","ITfFnShowHelp interface [Text Services Framework]","described","_tsf_itffnshowhelp_ref","ctffunc/ITfFnShowHelp","tsf.itffnshowhelp"]
old-location: tsf\itffnshowhelp.htm
tech.root: TSF
ms.assetid: d5d60767-95f3-4ed0-b61e-58e06d1e1a98
ms.date: 12/05/2018
ms.keywords: ITfFnShowHelp, ITfFnShowHelp interface [Text Services Framework], ITfFnShowHelp interface [Text Services Framework],described, _tsf_itffnshowhelp_ref, ctffunc/ITfFnShowHelp, tsf.itffnshowhelp
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfFnShowHelp
 - ctffunc/ITfFnShowHelp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfFnShowHelp
---

# ITfFnShowHelp interface


## -description

The <b>ITfFnShowHelp</b> interface is implemented by a text service to enable the language bar to place a help command for the text service in the language bar help menu.

## -inheritance

The <b>ITfFnShowHelp</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfFnShowHelp</b> also has these types of members:

## -remarks

The TSF manager obtains this interface from the text service by calling the text service <a href="/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction</a> interface with IID_ITfFnShowHelp.

The TSF manager obtains the help menu text by calling the text service's <a href="/windows/desktop/api/msctf/nf-msctf-itffunction-getdisplayname">ITfFunction::GetDisplayName</a>.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itffunction">ITfFunction
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itffunction-getdisplayname">ITfFunction::GetDisplayName
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
