---
UID: NF:tapi3if.ITTerminalSupport.get_StaticTerminals
title: ITTerminalSupport::get_StaticTerminals
author: windows-sdk-content
description: The get_StaticTerminals method creates a collection of currently available static terminals.
old-location: tapi3\itterminalsupport_get_staticterminals.htm
old-project: Tapi
ms.assetid: f4cdd3f5-ca8c-4660-b37c-c38779a516dd
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITTerminalSupport interface [TAPI 2.2],get_StaticTerminals method, ITTerminalSupport.get_StaticTerminals, ITTerminalSupport::get_StaticTerminals, _tapi3_itterminalsupport_get_staticterminals, get_StaticTerminals, get_StaticTerminals method [TAPI 2.2], get_StaticTerminals method [TAPI 2.2],ITTerminalSupport interface, tapi3.itterminalsupport_get_staticterminals, tapi3if/ITTerminalSupport::get_StaticTerminals
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tapi3if.h
api_name:
-	ITTerminalSupport.get_StaticTerminals
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTerminalSupport::get_StaticTerminals


## -description


The 
<b>get_StaticTerminals</b> method creates a collection of currently available static terminals. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/91fea706-9792-40e1-b812-f7578bc7968b">EnumerateStaticTerminals</a> method.


## -parameters




### -param pVariant [out]

Pointer to a <b>VARIANT</b>, which TAPI will fill in with an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface pointers.


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
The <i>pVariant</i> parameter is not a valid pointer.

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



TAPI calls the <a href="_com_iunknown_addref">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface returned by <b>ITTerminalSupport::get_StaticTerminals</b>. The application must call <a href="_com_iunknown_release">Release</a> on the 
<b>ITTerminal</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>



<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>



<a href="https://msdn.microsoft.com/8669324a-5c2c-4ed8-be24-a0c71fbb8c01">ITTerminalSupport</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>



<a href="https://msdn.microsoft.com/08320d1c-1400-4746-b526-74b0789c5fc0">Terminal Object Interfaces</a>
 

 

