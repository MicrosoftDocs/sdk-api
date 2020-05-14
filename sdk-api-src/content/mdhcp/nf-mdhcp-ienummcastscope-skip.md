---
UID: NF:mdhcp.IEnumMcastScope.Skip
title: IEnumMcastScope::Skip (mdhcp.h)
description: The Skip method skips over the next specified number of elements in the enumeration sequence.helpviewer_keywords: ["IEnumMcastScope interface [TAPI 2.2]","Skip method","IEnumMcastScope.Skip","IEnumMcastScope::Skip","Skip","Skip method [TAPI 2.2]","Skip method [TAPI 2.2]","IEnumMcastScope interface","_tapi3_ienummcastscope_skip","mdhcp/IEnumMcastScope::Skip","tapi3.ienummcastscope_skip"]
old-location: tapi3\ienummcastscope_skip.htm
tech.root: Tapi
ms.assetid: 0e2255e7-586b-422f-a500-a32e6a460514
ms.date: 12/05/2018
ms.keywords: IEnumMcastScope interface [TAPI 2.2],Skip method, IEnumMcastScope.Skip, IEnumMcastScope::Skip, Skip, Skip method [TAPI 2.2], Skip method [TAPI 2.2],IEnumMcastScope interface, _tapi3_ienummcastscope_skip, mdhcp/IEnumMcastScope::Skip, tapi3.ienummcastscope_skip
f1_keywords:
- mdhcp/IEnumMcastScope.Skip
dev_langs:
- c++
req.header: mdhcp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Mdhcp.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mdhcp.dll
api_name:
- IEnumMcastScope.Skip
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumMcastScope::Skip


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>Skip</b> method skips over the next specified number of elements in the enumeration sequence.


## -parameters




### -param celt [in]

Number of elements to skip.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Number of elements skipped was <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements skipped was not <i>celt</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nn-mdhcp-ienummcastscope">IEnumMcastScope</a>
 

 

