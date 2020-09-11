---
UID: NN:msctf.ITfClientId
title: ITfClientId (msctf.h)
description: The ITfClientId interface is implemented by the TSF manager. This interface is used to obtain a client identifier for TSF objects. An instance of this interface is obtained by querying the thread manager with IID_ITfClientId.
helpviewer_keywords: ["ITfClientId","ITfClientId interface [Text Services Framework]","ITfClientId interface [Text Services Framework]","described","_tsf_itfclientid_ref","msctf/ITfClientId","tsf.itfclientid"]
old-location: tsf\itfclientid.htm
tech.root: TSF
ms.assetid: ccb06ed3-67e2-4e46-8037-ff215ba23601
ms.date: 12/05/2018
ms.keywords: ITfClientId, ITfClientId interface [Text Services Framework], ITfClientId interface [Text Services Framework],described, _tsf_itfclientid_ref, msctf/ITfClientId, tsf.itfclientid
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfClientId
 - msctf/ITfClientId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfClientId
---

# ITfClientId interface


## -description

The <b>ITfClientId</b> interface is implemented by the TSF manager. This interface is used to obtain a client identifier for TSF objects. An instance of this interface is obtained by querying the thread manager with IID_ITfClientId.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfClientId</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfClientId</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfClientId</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfclientid-getclientid">GetClientId</a>
</td>
<td align="left" width="63%">
Obtains a client identifier for a CLSID.

</td>
</tr>
</table>

