---
UID: NN:msctf.ITfCompartmentMgr
title: ITfCompartmentMgr
author: windows-sdk-content
description: The ITfCompartmentMgr interface is implemented by the TSF manager and used by clients (applications and text services) to obtain and manipulate TSF compartments.
old-location: tsf\itfcompartmentmgr.htm
tech.root: TSF
ms.assetid: 7cdc5c82-4aac-4ec9-b791-93cea33ba8d2
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ITfCompartmentMgr, ITfCompartmentMgr interface [Text Services Framework], ITfCompartmentMgr interface [Text Services Framework],described, _tsf_itfcompartmentmgr_ref, msctf/ITfCompartmentMgr, tsf.itfcompartmentmgr
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# ITfCompartmentMgr interface


## -description


The <b>ITfCompartmentMgr</b> interface is implemented by the TSF manager and used by clients (applications and text services) to obtain and manipulate TSF compartments.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCompartmentMgr</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfCompartmentMgr</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/862ec077-b192-412a-b80c-6105f503ed21">ClearCompartment</a>
</td>
<td align="left" width="63%">
Removes the specified compartment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8c90637-dd6d-425f-9d5d-44c7dbfcf8a5">EnumCompartments</a>
</td>
<td align="left" width="63%">
Obtains an enumerator that contains the GUID of each compartment within the compartment manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f71815b-d352-4303-a3dd-180a71f9a5fe">GetCompartment</a>
</td>
<td align="left" width="63%">
Obtains the compartment object for a specified compartment.

</td>
</tr>
</table> 


## -remarks



The set of compartments that this interface is responsible for depends upon how the interface was obtained. An instance of this interface can be obtained in one of the following ways. For more information, see <a href="https://msdn.microsoft.com/7bffab6f-be40-4d3a-9342-6f81557a9656">Compartments</a>.

<ul>
<li>
<a href="https://msdn.microsoft.com/801e2c3a-0445-4630-83ba-55f51ef2704e">ITfThreadMgr::GetGlobalCompartment
            </a> - Obtains the global compartment manager.</li>
<li><b>ITfThreadMgr::QueryInterface</b> with IID_ITfCompartmentMgr - Obtains the compartment manager for this specific thread manager.</li>
<li><b>ITfDocumentMgr::QueryInterface</b> with IID_ITfCompartmentMgr - Obtains the compartment manager for this specific document manager.</li>
<li><b>ITfContext::QueryInterface</b> with IID_ITfCompartmentMgr - Obtains the compartment manager for this specific context.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/7bffab6f-be40-4d3a-9342-6f81557a9656">Compartments</a>



<a href="https://msdn.microsoft.com/801e2c3a-0445-4630-83ba-55f51ef2704e">ITfThreadMgr::GetGlobalCompartment
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

