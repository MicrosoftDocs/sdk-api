---
UID: NF:tapi3if.ITTerminalSupport.EnumerateStaticTerminals
title: ITTerminalSupport::EnumerateStaticTerminals (tapi3if.h)
author: windows-sdk-content
description: The EnumerateStaticTerminals method enumerates the currently available static terminals associated with the address.
old-location: tapi3\itterminalsupport_enumeratestaticterminals.htm
tech.root: Tapi
ms.assetid: 91fea706-9792-40e1-b812-f7578bc7968b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnumerateStaticTerminals, EnumerateStaticTerminals method [TAPI 2.2], EnumerateStaticTerminals method [TAPI 2.2],ITTerminalSupport interface, ITTerminalSupport interface [TAPI 2.2],EnumerateStaticTerminals method, ITTerminalSupport.EnumerateStaticTerminals, ITTerminalSupport::EnumerateStaticTerminals, _tapi3_itterminalsupport_enumeratestaticterminals, tapi3.itterminalsupport_enumeratestaticterminals, tapi3if/ITTerminalSupport::EnumerateStaticTerminals
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITTerminalSupport.EnumerateStaticTerminals
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTerminalSupport::EnumerateStaticTerminals


## -description


The 
<b>EnumerateStaticTerminals</b> method enumerates the currently available static terminals associated with the address. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="https://msdn.microsoft.com/f4cdd3f5-ca8c-4660-b37c-c38779a516dd">get_StaticTerminals</a> method.


## -parameters




### -param ppTerminalEnumerator [out]

Pointer to an 
<a href="https://msdn.microsoft.com/a364e466-1d10-402f-935d-ff2713522fed">IEnumTerminal</a> enumerator.


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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppTerminalEnumerator</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <a href="https://msdn.microsoft.com/en-us/library/ms691379(v=VS.85).aspx">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/a364e466-1d10-402f-935d-ff2713522fed">IEnumTerminal</a> interface returned by <b>ITTerminalSupport::EnumerateStaticTerminals</b>. The application must call <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">Release</a> on the 
<b>IEnumTerminal</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/8669324a-5c2c-4ed8-be24-a0c71fbb8c01">ITTerminalSupport</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>



<a href="https://msdn.microsoft.com/08320d1c-1400-4746-b526-74b0789c5fc0">Terminal Object Interfaces</a>
 

 

