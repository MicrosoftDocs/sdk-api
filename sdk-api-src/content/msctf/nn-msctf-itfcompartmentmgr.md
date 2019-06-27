---
UID: NN:msctf.ITfCompartmentMgr
title: ITfCompartmentMgr (msctf.h)
author: windows-sdk-content
description: The ITfCompartmentMgr interface is implemented by the TSF manager and used by clients (applications and text services) to obtain and manipulate TSF compartments.
old-location: tsf\itfcompartmentmgr.htm
tech.root: TSF
ms.assetid: 7cdc5c82-4aac-4ec9-b791-93cea33ba8d2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfCompartmentMgr, ITfCompartmentMgr interface [Text Services Framework], ITfCompartmentMgr interface [Text Services Framework],described, _tsf_itfcompartmentmgr_ref, msctf/ITfCompartmentMgr, tsf.itfcompartmentmgr
ms.topic: interface
f1_keywords: 
 - "msctf/ITfCompartmentMgr"
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
 - ITfCompartmentMgr
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfCompartmentMgr interface


## -description


The <b>ITfCompartmentMgr</b> interface is implemented by the TSF manager and used by clients (applications and text services) to obtain and manipulate TSF compartments.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCompartmentMgr</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfCompartmentMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfCompartmentMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcompartmentmgr-clearcompartment">ClearCompartment</a>
</td>
<td align="left" width="63%">
Removes the specified compartment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcompartmentmgr-enumcompartments">EnumCompartments</a>
</td>
<td align="left" width="63%">
Obtains an enumerator that contains the GUID of each compartment within the compartment manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcompartmentmgr-getcompartment">GetCompartment</a>
</td>
<td align="left" width="63%">
Obtains the compartment object for a specified compartment.

</td>
</tr>
</table> 


## -remarks



The set of compartments that this interface is responsible for depends upon how the interface was obtained. An instance of this interface can be obtained in one of the following ways. For more information, see <a href="https://docs.microsoft.com/windows/desktop/TSF/compartments">Compartments</a>.

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-getglobalcompartment">ITfThreadMgr::GetGlobalCompartment
            </a> - Obtains the global compartment manager.</li>
<li><b>ITfThreadMgr::QueryInterface</b> with IID_ITfCompartmentMgr - Obtains the compartment manager for this specific thread manager.</li>
<li><b>ITfDocumentMgr::QueryInterface</b> with IID_ITfCompartmentMgr - Obtains the compartment manager for this specific document manager.</li>
<li><b>ITfContext::QueryInterface</b> with IID_ITfCompartmentMgr - Obtains the compartment manager for this specific context.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TSF/compartments">Compartments</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-getglobalcompartment">ITfThreadMgr::GetGlobalCompartment
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

