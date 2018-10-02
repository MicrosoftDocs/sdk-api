---
UID: NF:mergemod.IMsmMerge.get_Errors
title: IMsmMerge::get_Errors
author: windows-sdk-content
description: The get_Errors method retrieves the Errors property of the Merge object. This retrieves the current collection of errors.
old-location: setup\imsmmerge_get_errors.htm
tech.root: MSI
ms.assetid: 81bf84f6-d469-47b1-9097-8a3ee9c8550d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMsmMerge interface,get_Errors method, IMsmMerge.get_Errors, IMsmMerge::get_Errors, _msi_get_errors_function, get_Errors, get_Errors method, get_Errors method,IMsmMerge interface, mergemod/IMsmMerge::get_Errors, setup.imsmmerge_get_errors
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
req.dll: Mergemod.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmMerge.get_Errors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMsmMerge::get_Errors


## -description


The 
<b>get_Errors</b> method retrieves the 
<a href="https://msdn.microsoft.com/619f17cc-131a-4262-ad48-9ab1318142aa">Errors</a> property of the 
<a href="https://msdn.microsoft.com/3f76ee8a-d195-4a69-99a3-31ef2c1c72d5">Merge</a> object. This retrieves the current collection of errors.

<b>IMsmMerge2::get_Errors</b>    Mergemod.dll version 2.0 or later.<div> </div><b>IMsmMerge::get_Errors</b>      All Mergemod.dll versions.
			


## -parameters




### -param Errors [out]

Pointer to a memory location containing another pointer to an <b>IMsmErrors</b> interface.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>Errors</i> pointer is <b>NULL</b>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



The retrieval is non-destructive, meaning that several instances of the error collection may be retrieved by repeatedly calling this method.

If there is an error, the memory location pointed to by <i>Errors</i> is set to <b>NULL</b>.

The client is responsible for releasing the interface returned by this function.




## -see-also




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

