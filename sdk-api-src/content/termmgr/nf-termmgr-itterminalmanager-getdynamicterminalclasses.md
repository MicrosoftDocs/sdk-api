---
UID: NF:termmgr.ITTerminalManager.GetDynamicTerminalClasses
title: ITTerminalManager::GetDynamicTerminalClasses
author: windows-sdk-content
description: The GetDynamicTerminalClasses method gets a list of terminal classes for a set of media types.
old-location: tapi3\itterminalmanager_getdynamicterminalclasses.htm
tech.root: TAPI
ms.assetid: 6e0ae94c-eab9-4ca2-a982-a5673f73130e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetDynamicTerminalClasses, GetDynamicTerminalClasses method [TAPI 2.2], GetDynamicTerminalClasses method [TAPI 2.2],ITTerminalManager interface, ITTerminalManager interface [TAPI 2.2],GetDynamicTerminalClasses method, ITTerminalManager.GetDynamicTerminalClasses, ITTerminalManager::GetDynamicTerminalClasses, _tapi3_itterminalmanager_getdynamicterminalclasses, tapi3.itterminalmanager_getdynamicterminalclasses, termmgr/ITTerminalManager::GetDynamicTerminalClasses
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: termmgr.h
req.include-header: 
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
 - Termmgr.h
api_name:
 - ITTerminalManager.GetDynamicTerminalClasses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTerminalManager::GetDynamicTerminalClasses


## -description


The 
<b>GetDynamicTerminalClasses</b> method gets a list of terminal classes for a set of media types.


## -parameters




### -param dwMediaTypes [in]

Pointer to 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media types</a>.


### -param pdwNumClasses [in, out]

Number of terminal classes returned.


### -param pTerminalClasses [out]

Pointer to list of 
<a href="https://msdn.microsoft.com/2a16d33c-2d87-4172-a5ff-33ff62e96615">terminal classes</a>.


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
The <i>pdwNumClasses</i> or the <i>pTerminalClasses</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NOTENOUGHMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Dynamic terminals not supported on this address.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7e5bd83d-42c5-463c-8ce0-c6f466f60588">ITTerminalManager</a>
 

 

