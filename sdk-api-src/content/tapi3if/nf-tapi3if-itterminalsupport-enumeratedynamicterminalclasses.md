---
UID: NF:tapi3if.ITTerminalSupport.EnumerateDynamicTerminalClasses
title: ITTerminalSupport::EnumerateDynamicTerminalClasses
author: windows-sdk-content
description: The EnumerateDynamicTerminalClasses method enumerates the currently available dynamic terminal classes that are supported.
old-location: tapi3\itterminalsupport_enumeratedynamicterminalclasses.htm
old-project: tapi
ms.assetid: 1dcb9163-306b-42fc-afb4-41b33d7e2d40
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: EnumerateDynamicTerminalClasses, EnumerateDynamicTerminalClasses method [TAPI 2.2], EnumerateDynamicTerminalClasses method [TAPI 2.2],ITTerminalSupport interface, ITTerminalSupport interface [TAPI 2.2],EnumerateDynamicTerminalClasses method, ITTerminalSupport.EnumerateDynamicTerminalClasses, ITTerminalSupport::EnumerateDynamicTerminalClasses, _tapi3_itterminalsupport_enumeratedynamicterminalclasses, tapi3.itterminalsupport_enumeratedynamicterminalclasses, tapi3if/ITTerminalSupport::EnumerateDynamicTerminalClasses
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
 - ITTerminalSupport.EnumerateDynamicTerminalClasses
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTerminalSupport::EnumerateDynamicTerminalClasses


## -description


The 
<b>EnumerateDynamicTerminalClasses</b> method enumerates the currently available dynamic 
<a href="https://msdn.microsoft.com/2a16d33c-2d87-4172-a5ff-33ff62e96615">terminal classes</a> that are supported. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="https://msdn.microsoft.com/258fad5c-6269-45ab-bdc0-d38338f8e515">get_DynamicTerminalClasses</a> method.


## -parameters




### -param ppTerminalClassEnumerator [out]

Pointer to an 
<a href="https://msdn.microsoft.com/1da0a82a-fde4-440c-ac6c-e9b85a7ec3fe">IEnumTerminalClass</a> enumerator. TAPI returns these classes as GUIDs.


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
The <i>ppTerminalClassEnumerator</i> parameter is not a valid pointer.

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



An application calls this method to find out which dynamic terminal classes are supported by this address in a call to 
<a href="https://msdn.microsoft.com/2a2a037a-753c-4dd4-b6ce-10b69f2e2421">ITTerminalSupport::CreateTerminal</a>.

TAPI calls the <a href="https://msdn.microsoft.com/en-us/library/ms691379(v=VS.85).aspx">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/1da0a82a-fde4-440c-ac6c-e9b85a7ec3fe">IEnumTerminalClass</a> interface returned by <b>ITTerminalSupport::EnumerateDynamicTerminalClasses</b>. The application must call <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">Release</a> on the 
<b>IEnumTerminalClass</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/8669324a-5c2c-4ed8-be24-a0c71fbb8c01">ITTerminalSupport</a>



<b>Terminal Classes</b>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>



<a href="https://msdn.microsoft.com/08320d1c-1400-4746-b526-74b0789c5fc0">Terminal Object Interfaces</a>



<a href="https://msdn.microsoft.com/2a16d33c-2d87-4172-a5ff-33ff62e96615">terminal classes</a>
 

 

