---
UID: NF:tapi3if.ITTerminalSupport.get_DynamicTerminalClasses
title: ITTerminalSupport::get_DynamicTerminalClasses
author: windows-sdk-content
description: The get_DynamicTerminalClasses method creates a collection of currently available dynamic terminals.
old-location: tapi3\itterminalsupport_get_dynamicterminalclasses.htm
tech.root: tapi
ms.assetid: 258fad5c-6269-45ab-bdc0-d38338f8e515
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITTerminalSupport interface [TAPI 2.2],get_DynamicTerminalClasses method, ITTerminalSupport.get_DynamicTerminalClasses, ITTerminalSupport::get_DynamicTerminalClasses, _tapi3_itterminalsupport_get_dynamicterminalclasses, get_DynamicTerminalClasses, get_DynamicTerminalClasses method [TAPI 2.2], get_DynamicTerminalClasses method [TAPI 2.2],ITTerminalSupport interface, tapi3.itterminalsupport_get_dynamicterminalclasses, tapi3if/ITTerminalSupport::get_DynamicTerminalClasses
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
 - ITTerminalSupport.get_DynamicTerminalClasses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTerminalSupport::get_DynamicTerminalClasses


## -description


The 
<b>get_DynamicTerminalClasses</b> method creates a collection of currently available dynamic terminals. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/1dcb9163-306b-42fc-afb4-41b33d7e2d40">EnumerateDynamicTerminalClasses</a> method.


## -parameters




### -param pVariant [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/2a16d33c-2d87-4172-a5ff-33ff62e96615">terminal classes</a> in a string (<b>BSTR</b>) format.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

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
</table>
 




## -remarks



An application calls this method to find out which dynamic terminal classes are supported by this address in a call to 
<a href="https://msdn.microsoft.com/2a2a037a-753c-4dd4-b6ce-10b69f2e2421">ITTerminalSupport::CreateTerminal</a>.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/8669324a-5c2c-4ed8-be24-a0c71fbb8c01">ITTerminalSupport</a>



<a href="https://msdn.microsoft.com/2a16d33c-2d87-4172-a5ff-33ff62e96615">Terminal Class</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>



<a href="https://msdn.microsoft.com/08320d1c-1400-4746-b526-74b0789c5fc0">Terminal Object Interfaces</a>
 

 

