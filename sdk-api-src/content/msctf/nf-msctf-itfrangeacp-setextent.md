---
UID: NF:msctf.ITfRangeACP.SetExtent
title: ITfRangeACP::SetExtent (msctf.h)
author: windows-sdk-content
description: ITfRangeACP::SetExtent method
old-location: tsf\itfrangeacp_setextent.htm
tech.root: TSF
ms.assetid: 7b409ba8-dce6-4b42-8cfe-f159de1cad2c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfRangeACP interface [Text Services Framework],SetExtent method, ITfRangeACP.SetExtent, ITfRangeACP::SetExtent, SetExtent, SetExtent method [Text Services Framework], SetExtent method [Text Services Framework],ITfRangeACP interface, _tsf_itfrangeacp_setextent_ref, msctf/ITfRangeACP::SetExtent, tsf.itfrangeacp_setextent
ms.topic: method
f1_keywords: 
 - "msctf/ITfRangeACP.SetExtent"
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
 - ITfRangeACP.SetExtent
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfRangeACP::SetExtent


## -description




## -parameters




### -param acpAnchor [in]

Contains the application character position of the range start anchor.


### -param cch [in]

Contains the number of characters in the range.


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




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfrangeacp">ITfRangeACP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrangeacp-getextent">ITfRangeACP::GetExtent
      </a>
 

 

