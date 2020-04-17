---
UID: NN:msctf.ITfFunction
title: ITfFunction (msctf.h)
description: The ITfFunction interface is the base interface for the individual function interfaces.helpviewer_keywords: ["ITfFunction","ITfFunction interface [Text Services Framework]","ITfFunction interface [Text Services Framework]","described","_tsf_itffunction_ref","msctf/ITfFunction","tsf.itffunction"]
old-location: tsf\itffunction.htm
tech.root: TSF
ms.assetid: 140b1ed8-8876-4f06-8ed2-7b0dccdc0a69
ms.date: 12/05/2018
ms.keywords: ITfFunction, ITfFunction interface [Text Services Framework], ITfFunction interface [Text Services Framework],described, _tsf_itffunction_ref, msctf/ITfFunction, tsf.itffunction
f1_keywords:
- msctf/ITfFunction
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
req.dll: Msctf.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msctf.dll
api_name:
- ITfFunction
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfFunction interface


## -description


The <b>ITfFunction</b> interface is the base interface for the individual function interfaces. This interface is implemented by the provider of the function object and used by any component to obtain the display name of the function object. Instances of this interface are not obtained directly. This interface is always part of a derived interface, such as <a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nn-ctffunc-itffnshowhelp">ITfFnShowHelp</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFunction</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfFunction</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFunction</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itffunction-getdisplayname">GetDisplayName</a>
</td>
<td align="left" width="63%">
Obtains the function display name.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nn-ctffunc-itffnshowhelp">ITfFnShowHelp
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

