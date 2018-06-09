---
UID: NN:msctf.ITfCompartment
title: ITfCompartment
author: windows-sdk-content
description: The ITfCompartment interface is implemented by the TSF manager and is used by clients (applications and text services) to obtain and set data in a TSF compartment.
old-location: tsf\itfcompartment.htm
old-project: TSF
ms.assetid: c9ca3eb5-1fb1-4e45-9ec4-a0296f1bc8c3
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITfCompartment, ITfCompartment interface [Text Services Framework], ITfCompartment interface [Text Services Framework],described, _tsf_itfcompartment_ref, msctf/ITfCompartment, tsf.itfcompartment
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
 - msctf.dll
api_name:
 - ITfCompartment
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfCompartment interface


## -description


The <b>ITfCompartment</b> interface is implemented by the TSF manager and is used by clients (applications and text services) to obtain and set data in a TSF compartment.

A client also uses this interface to obtain an <a href="https://msdn.microsoft.com/2ff77f09-1b4c-4115-9bb4-4040097d1f90">ITfSource</a> interface that is used to install an <a href="https://msdn.microsoft.com/1bd464e7-9e34-4725-83f9-42e09ddf4778">ITfCompartmentEventSink</a> compartment change notification sink. The client calls <b>ITfCompartment::QueryInterface</b> with IID_ITfSource to obtain the <b>ITfSource</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCompartment</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfCompartment</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597624">GetValue</a>
</td>
<td align="left" width="63%">
Obtains the data for a compartment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a>
</td>
<td align="left" width="63%">
Sets the data for a compartment.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/7bffab6f-be40-4d3a-9342-6f81557a9656">Compartments</a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

