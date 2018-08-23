---
UID: NF:rend.IEnumDialableAddrs.Next
title: IEnumDialableAddrs::Next
author: windows-sdk-content
description: The Next method gets the next specified number of elements in the enumeration sequence.
old-location: tapi3\ienumdialableaddrs_next.htm
old-project: tapi
ms.assetid: 78ebe1d3-3c40-4ba4-97f0-8612775c80f0
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: IEnumDialableAddrs interface [TAPI 2.2],Next method, IEnumDialableAddrs.Next, IEnumDialableAddrs::Next, Next, Next method [TAPI 2.2], Next method [TAPI 2.2],IEnumDialableAddrs interface, _tapi3_ienumdialableaddrs_next, rend/IEnumDialableAddrs::Next, tapi3.ienumdialableaddrs_next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rend.h
req.include-header: 
req.redist: 
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
 - IEnumDialableAddrs.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: ADAM
---

# IEnumDialableAddrs::Next


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>Next</b> method gets the next specified number of elements in the enumeration sequence.


## -parameters




### -param celt [in]

Number of elements requested.


### -param ppElements [out]

Pointer to a <b>BSTR</b> representation of the address list.


### -param pcFetched [out]

Pointer to the number of elements actually supplied. May be <b>NULL</b> if <i>celt</i> is one.


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
Method returned <i>celt</i> number of elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements remaining was less than <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppElements</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



The application must use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory allocated for the <i>ppElements</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/0a64cb89-9e44-4af1-9b0f-2eec6e5267c7">IEnumDialableAddrs</a>
 

 

