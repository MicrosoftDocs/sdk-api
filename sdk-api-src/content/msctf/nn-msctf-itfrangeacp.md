---
UID: NN:msctf.ITfRangeACP
title: ITfRangeACP
author: windows-sdk-content
description: The ITfRangeACP interface is implemented by the TSF manager and is used by an application character position (ACP)-based application to access and manipulate range objects.
old-location: tsf\itfrangeacp.htm
tech.root: TSF
ms.assetid: aaa497ca-4cf2-401a-a6d8-cc8a75479cc4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfRangeACP, ITfRangeACP interface [Text Services Framework], ITfRangeACP interface [Text Services Framework],described, _tsf_itfrangeacp_ref, msctf/ITfRangeACP, tsf.itfrangeacp
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITfRangeACP
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfRangeACP interface


## -description


The <b>ITfRangeACP</b> interface is implemented by the TSF manager and is used by an application character position (ACP)-based application to access and manipulate range objects. This interface is derived from the <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> interface. Obtain an instance of this interface by querying an <b>ITfRange</b> object for IID_ITfRangeACP.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfRangeACP</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfRangeACP</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfRangeACP</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14838cea-1a19-4faa-ac7f-617fde82432d">GetExtent</a>
</td>
<td align="left" width="63%">
Obtains the application character position and length of the range object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b409ba8-dce6-4b42-8cfe-f159de1cad2c">SetExtent</a>
</td>
<td align="left" width="63%">
Sets the application character position and length of the range object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

