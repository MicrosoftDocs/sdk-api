---
UID: NN:ctffunc.ITfFnShowHelp
title: ITfFnShowHelp (ctffunc.h)
description: The ITfFnShowHelp interface is implemented by a text service to enable the language bar to place a help command for the text service in the language bar help menu.
old-location: tsf\itffnshowhelp.htm
tech.root: TSF
ms.assetid: d5d60767-95f3-4ed0-b61e-58e06d1e1a98
ms.date: 12/05/2018
ms.keywords: ITfFnShowHelp, ITfFnShowHelp interface [Text Services Framework], ITfFnShowHelp interface [Text Services Framework],described, _tsf_itffnshowhelp_ref, ctffunc/ITfFnShowHelp, tsf.itffnshowhelp
ms.topic: interface
f1_keywords:
- ctffunc/ITfFnShowHelp
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Msctf.dll
api_name:
- ITfFnShowHelp
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfFnShowHelp interface


## -description


The <b>ITfFnShowHelp</b> interface is implemented by a text service to enable the language bar to place a help command for the text service in the language bar help menu.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnShowHelp</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfFnShowHelp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFnShowHelp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itffnshowhelp-show">Show</a>
</td>
<td align="left" width="63%">
Called when the user selects a text service help menu item.

</td>
</tr>
</table> 


## -remarks



The TSF manager obtains this interface from the text service by calling the text service <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction</a> interface with IID_ITfFnShowHelp.

The TSF manager obtains the help menu text by calling the text service's <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itffunction-getdisplayname">ITfFunction::GetDisplayName</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itffunction">ITfFunction
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itffunction-getdisplayname">ITfFunction::GetDisplayName
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

