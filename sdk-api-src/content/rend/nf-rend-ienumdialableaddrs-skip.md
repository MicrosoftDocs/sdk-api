---
UID: NF:rend.IEnumDialableAddrs.Skip
title: IEnumDialableAddrs::Skip
author: windows-sdk-content
description: The Skip method skips over the next specified number of elements in the enumeration sequence.
old-location: tapi3\ienumdialableaddrs_skip.htm
tech.root: TAPI
ms.assetid: f68fa12d-dbd3-42a2-bef1-50881d57aa27
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IEnumDialableAddrs interface [TAPI 2.2],Skip method, IEnumDialableAddrs.Skip, IEnumDialableAddrs::Skip, Skip, Skip method [TAPI 2.2], Skip method [TAPI 2.2],IEnumDialableAddrs interface, _tapi3_ienumdialableaddrs_skip, rend/IEnumDialableAddrs::Skip, tapi3.ienumdialableaddrs_skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rend.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rend.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Rend.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - IEnumDialableAddrs.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumDialableAddrs::Skip


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




<a href="https://msdn.microsoft.com/0a64cb89-9e44-4af1-9b0f-2eec6e5267c7">IEnumDialableAddrs</a>
 

 

