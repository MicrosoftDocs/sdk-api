---
UID: NF:rend.IEnumDirectory.Skip
title: IEnumDirectory::Skip
author: windows-sdk-content
description: The Skip method skips over the next specified number of elements in the enumeration sequence.
old-location: tapi3\ienumdirectory_skip.htm
old-project: tapi
ms.assetid: 45694bee-52d8-4a44-bc14-b9d03355bce1
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: IEnumDirectory interface [TAPI 2.2],Skip method, IEnumDirectory.Skip, IEnumDirectory::Skip, Skip, Skip method [TAPI 2.2], Skip method [TAPI 2.2],IEnumDirectory interface, _tapi3_ienumdirectory_skip, rend/IEnumDirectory::Skip, tapi3.ienumdirectory_skip
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RND_ADVERTISING_SCOPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - IEnumDirectory.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: ADAM
---

# IEnumDirectory::Skip


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
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




<a href="https://msdn.microsoft.com/9c1e83c5-c718-4a3b-916d-e844a8377a29">IEnumDirectory</a>
 

 

