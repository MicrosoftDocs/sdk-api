---
UID: NN:msctf.ITfCompartment
title: ITfCompartment (msctf.h)
author: windows-sdk-content
description: The ITfCompartment interface is implemented by the TSF manager and is used by clients (applications and text services) to obtain and set data in a TSF compartment.
old-location: tsf\itfcompartment.htm
tech.root: TSF
ms.assetid: c9ca3eb5-1fb1-4e45-9ec4-a0296f1bc8c3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfCompartment, ITfCompartment interface [Text Services Framework], ITfCompartment interface [Text Services Framework],described, _tsf_itfcompartment_ref, msctf/ITfCompartment, tsf.itfcompartment
ms.topic: interface
f1_keywords: ["msctf/ITfCompartment"]
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
 - ITfCompartment
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfCompartment interface


## -description


The <b>ITfCompartment</b> interface is implemented by the TSF manager and is used by clients (applications and text services) to obtain and set data in a TSF compartment.

A client also uses this interface to obtain an <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource</a> interface that is used to install an <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcompartmenteventsink">ITfCompartmentEventSink</a> compartment change notification sink. The client calls <b>ITfCompartment::QueryInterface</b> with IID_ITfSource to obtain the <b>ITfSource</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCompartment</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfCompartment</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfCompartment</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcompartment-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Obtains the data for a compartment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcompartment-setvalue">SetValue</a>
</td>
<td align="left" width="63%">
Sets the data for a compartment.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TSF/compartments">Compartments</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

