---
UID: NF:termmgr.ITTerminalManager2.GetPluggableSuperclasses
title: ITTerminalManager2::GetPluggableSuperclasses
author: windows-sdk-content
description: The GetPluggableSuperclasses method gets the public CLSIDs for all pluggable terminal superclasses in the registry.
old-location: tapi3\itterminalmanager2_getpluggablesuperclasses.htm
old-project: Tapi
ms.assetid: a3db1979-0ba5-416a-bb14-0ac4b61eb425
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: GetPluggableSuperclasses, GetPluggableSuperclasses method [TAPI 2.2], GetPluggableSuperclasses method [TAPI 2.2],ITTerminalManager2 interface, ITTerminalManager2 interface [TAPI 2.2],GetPluggableSuperclasses method, ITTerminalManager2.GetPluggableSuperclasses, ITTerminalManager2::GetPluggableSuperclasses, _tapi3_itterminalmanager2_getpluggablesuperclasses, tapi3.itterminalmanager2_getpluggablesuperclasses, termmgr/ITTerminalManager2::GetPluggableSuperclasses
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: TMGR_DIRECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Termmgr.h
api_name:
-	ITTerminalManager2.GetPluggableSuperclasses
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTerminalManager2::GetPluggableSuperclasses


## -description


The 
<b>GetPluggableSuperclasses</b> method gets the public CLSIDs for all pluggable terminal superclasses in the registry.


## -parameters




### -param pdwNumSuperclasses [in, out]

The number of superclasses retrieved. If <i>pSuperclasses</i> is <b>NULL</b>, this argument is used to get the total number of pluggable terminal superclasses registered in the registry. If <i>pSuperclasses</i> is not <b>NULL</b>, this argument is used to pass the size, in IIDs, of the <i>pSuperclasses</i> buffer, and the method returns the number of IIDs copied into buffer memory.


### -param pSuperclasses [out]

Pointer to an IID buffer allocated by the user. 




If the buffer is <b>NULL</b>, the method returns the count of superclasses in the buffer. Otherwise, the method returns the IIDs of the pluggable terminal superclasses registered on the system.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Method failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f91c8684-27f8-4db8-99ff-d5a6cb87a0c2">ITTerminalManager2</a>
 

 

