---
UID: NF:tapi3if.ITTerminalSupport.CreateTerminal
title: ITTerminalSupport::CreateTerminal
author: windows-sdk-content
description: The CreateTerminal method creates and initializes a new ITTerminal object based on the dynamic terminal class and media. The terminal class is identified by a GUID. The GUID must be converted to a string using StringFromIID to pass to this method.
old-location: tapi3\itterminalsupport_createterminal.htm
old-project: Tapi
ms.assetid: 2a2a037a-753c-4dd4-b6ce-10b69f2e2421
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: CreateTerminal, CreateTerminal method [TAPI 2.2], CreateTerminal method [TAPI 2.2],ITTerminalSupport interface, ITTerminalSupport interface [TAPI 2.2],CreateTerminal method, ITTerminalSupport.CreateTerminal, ITTerminalSupport::CreateTerminal, _tapi3_itterminalsupport_createterminal, tapi3.itterminalsupport_createterminal, tapi3if/ITTerminalSupport::CreateTerminal
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITTerminalSupport.CreateTerminal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTerminalSupport::CreateTerminal


## -description


The 
<b>CreateTerminal</b> method creates and initializes a new 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> object based on the dynamic terminal class and media. The 
<a href="https://msdn.microsoft.com/2a16d33c-2d87-4172-a5ff-33ff62e96615">terminal class</a> is identified by a GUID. The GUID must be converted to a string using 
<a href="https://msdn.microsoft.com/library/ms688692(v=VS.85).aspx">StringFromIID</a> to pass to this method.


## -parameters




### -param pTerminalClass [in]

Pointer to <b>BSTR</b> containing the 
<a href="https://msdn.microsoft.com/2a16d33c-2d87-4172-a5ff-33ff62e96615">terminal class</a> (GUID) for the new terminal object.


### -param lMediaType [in]

Pointer to the 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a> for the new terminal object.


### -param Direction [in]


<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">TERMINAL_DIRECTION</a> descriptor of the terminal direction.


### -param ppTerminal [out]

Pointer to the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> object created.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pTerminalClass</i> or <i>lMediaType</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppTerminal</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to create the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
The <i>lMediaType</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Dynamic terminal creation is not supported.

</td>
</tr>
</table>
 




## -remarks



The application must use 
<a href="https://msdn.microsoft.com/library/ms221458(v=VS.85).aspx">SysAllocString</a> to allocate memory for the <i>pTerminalClass</i> parameter and use 
<a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory when the variable is no longer needed.

Once a terminal is created, it can be selected onto only one call.

TAPI calls the <a href="https://msdn.microsoft.com/library/Dd757100(v=VS.85).aspx">AddRef</a> method on the 
<b>ITTerminal</b> interface returned by <b>ITTerminalSupport::CreateTerminal</b>. The application must call <a href="https://msdn.microsoft.com/library/Dd757102(v=VS.85).aspx">Release</a> on the 
<b>ITTerminal</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/8669324a-5c2c-4ed8-be24-a0c71fbb8c01">ITTerminalSupport</a>



<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">TERMINAL_DIRECTION</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>



<a href="https://msdn.microsoft.com/08320d1c-1400-4746-b526-74b0789c5fc0">Terminal Object Interfaces</a>



<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a>



<a href="https://msdn.microsoft.com/2a16d33c-2d87-4172-a5ff-33ff62e96615">terminal class</a>
 

 

