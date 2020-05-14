---
UID: NN:msctf.ITfTransitoryExtensionSink
title: ITfTransitoryExtensionSink (msctf.h)
description: The ITfTransitoryExtensionSink interface is implemented by the application that uses Transitory Extension dim. The application can track the changes that happened in the transitory extension by using this sink interface.helpviewer_keywords: ["ITfTransitoryExtensionSink","ITfTransitoryExtensionSink interface [Text Services Framework]","ITfTransitoryExtensionSink interface [Text Services Framework]","described","_tsf_itftransitoryextensionsink_ref","msctf/ITfTransitoryExtensionSink","tsf.itftransitoryextensionsink"]
old-location: tsf\itftransitoryextensionsink.htm
tech.root: TSF
ms.assetid: c2c11bd9-ae33-462e-8534-dc57a5131846
ms.date: 12/05/2018
ms.keywords: ITfTransitoryExtensionSink, ITfTransitoryExtensionSink interface [Text Services Framework], ITfTransitoryExtensionSink interface [Text Services Framework],described, _tsf_itftransitoryextensionsink_ref, msctf/ITfTransitoryExtensionSink, tsf.itftransitoryextensionsink
f1_keywords:
- msctf/ITfTransitoryExtensionSink
dev_langs:
- c++
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Msctf.h
api_name:
- ITfTransitoryExtensionSink
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfTransitoryExtensionSink interface


## -description


The <b>ITfTransitoryExtensionSink</b> interface is implemented by the application that uses Transitory Extension dim. The application can track the changes that happened in the transitory extension by using this sink interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfTransitoryExtensionSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfTransitoryExtensionSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfTransitoryExtensionSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itftransitoryextensionsink-ontransitoryextensionupdated">OnTransitoryExtensionUpdated</a>
</td>
<td align="left" width="63%">Transitory Document has been updated.</td>
</tr>
</table> 

