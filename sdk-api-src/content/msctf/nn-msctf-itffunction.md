---
UID: NN:msctf.ITfFunction
title: ITfFunction
author: windows-sdk-content
description: The ITfFunction interface is the base interface for the individual function interfaces.
old-location: tsf\itffunction.htm
old-project: TSF
ms.assetid: 140b1ed8-8876-4f06-8ed2-7b0dccdc0a69
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITfFunction, ITfFunction interface [Text Services Framework], ITfFunction interface [Text Services Framework],described, _tsf_itffunction_ref, msctf/ITfFunction, tsf.itffunction
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
 - ITfFunction
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfFunction interface


## -description


The <b>ITfFunction</b> interface is the base interface for the individual function interfaces. This interface is implemented by the provider of the function object and used by any component to obtain the display name of the function object. Instances of this interface are not obtained directly. This interface is always part of a derived interface, such as <a href="https://msdn.microsoft.com/d5d60767-95f3-4ed0-b61e-58e06d1e1a98">ITfFnShowHelp</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFunction</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfFunction</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/da52ca6d-9606-45c5-8db9-c876c827df14">GetDisplayName</a>
</td>
<td align="left" width="63%">
Obtains the function display name.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d5d60767-95f3-4ed0-b61e-58e06d1e1a98">ITfFnShowHelp
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

