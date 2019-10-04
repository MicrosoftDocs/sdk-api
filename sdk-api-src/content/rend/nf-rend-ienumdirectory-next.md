---
UID: NF:rend.IEnumDirectory.Next
title: IEnumDirectory::Next (rend.h)
author: windows-sdk-content
description: The Next method gets the next specified number of elements in the enumeration sequence.
old-location: tapi3\ienumdirectory_next.htm
tech.root: Tapi
ms.assetid: db164275-92dc-4a25-ba19-fd26415624f1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumDirectory interface [TAPI 2.2],Next method, IEnumDirectory.Next, IEnumDirectory::Next, Next, Next method [TAPI 2.2], Next method [TAPI 2.2],IEnumDirectory interface, _tapi3_ienumdirectory_next, rend/IEnumDirectory::Next, tapi3.ienumdirectory_next
ms.topic: method
f1_keywords: 
 - "rend/IEnumDirectory.Next"
dev_langs:
 - c++
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
 - IEnumDirectory.Next
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumDirectory::Next


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>Next</b> method gets the next specified number of elements in the enumeration sequence.


## -parameters




### -param celt [in]

Number of elements requested.


### -param ppElements [out]

Pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a> interface.


### -param pcFetched [out]

Pointer to the number of elements actually supplied. May be <b>NULL</b> if <i>celt</i> is one.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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



TAPI calls the <b>AddRef</b> method on the 
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a> interface returned by <b>IEnumDirectory::Next</b>. The application must call <b>Release</b> on the 
<b>ITDirectory</b> interface to free resources associated with it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rend/nn-rend-ienumdirectory">IEnumDirectory</a>
 

 

