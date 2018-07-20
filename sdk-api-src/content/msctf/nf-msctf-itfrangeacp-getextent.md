---
UID: NF:msctf.ITfRangeACP.GetExtent
title: ITfRangeACP::GetExtent
author: windows-sdk-content
description: ITfRangeACP::GetExtent method
old-location: tsf\itfrangeacp_getextent.htm
old-project: TSF
ms.assetid: 14838cea-1a19-4faa-ac7f-617fde82432d
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: GetExtent, GetExtent method [Text Services Framework], GetExtent method [Text Services Framework],ITfRangeACP interface, ITfRangeACP interface [Text Services Framework],GetExtent method, ITfRangeACP.GetExtent, ITfRangeACP::GetExtent, _tsf_itfrangeacp_getextent_ref, msctf/ITfRangeACP::GetExtent, tsf.itfrangeacp_getextent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - ITfRangeACP.GetExtent
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfRangeACP::GetExtent


## -description




## -parameters




### -param pacpAnchor [out]

Pointer to a <b>LONG</b> value that receives the application character position of the range start anchor.


### -param pcch [out]

Pointer to a <b>LONG</b> value that receives the number of characters in the range.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



This method should only be called by the owner of the ACP-based context because the character position and range length will only have meaning to a caller that recognizes the text store implementation.




## -see-also




<a href="https://msdn.microsoft.com/aaa497ca-4cf2-401a-a6d8-cc8a75479cc4">ITfRangeACP</a>



<a href="https://msdn.microsoft.com/7b409ba8-dce6-4b42-8cfe-f159de1cad2c">ITfRangeACP::SetExtent
      </a>
 

 

