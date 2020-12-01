---
UID: NF:termmgr.ITTerminalManager2.GetPluggableSuperclasses
title: ITTerminalManager2::GetPluggableSuperclasses (termmgr.h)
description: The GetPluggableSuperclasses method gets the public CLSIDs for all pluggable terminal superclasses in the registry.
helpviewer_keywords: ["GetPluggableSuperclasses","GetPluggableSuperclasses method [TAPI 2.2]","GetPluggableSuperclasses method [TAPI 2.2]","ITTerminalManager2 interface","ITTerminalManager2 interface [TAPI 2.2]","GetPluggableSuperclasses method","ITTerminalManager2.GetPluggableSuperclasses","ITTerminalManager2::GetPluggableSuperclasses","_tapi3_itterminalmanager2_getpluggablesuperclasses","tapi3.itterminalmanager2_getpluggablesuperclasses","termmgr/ITTerminalManager2::GetPluggableSuperclasses"]
old-location: tapi3\itterminalmanager2_getpluggablesuperclasses.htm
tech.root: tapi3
ms.assetid: a3db1979-0ba5-416a-bb14-0ac4b61eb425
ms.date: 12/05/2018
ms.keywords: GetPluggableSuperclasses, GetPluggableSuperclasses method [TAPI 2.2], GetPluggableSuperclasses method [TAPI 2.2],ITTerminalManager2 interface, ITTerminalManager2 interface [TAPI 2.2],GetPluggableSuperclasses method, ITTerminalManager2.GetPluggableSuperclasses, ITTerminalManager2::GetPluggableSuperclasses, _tapi3_itterminalmanager2_getpluggablesuperclasses, tapi3.itterminalmanager2_getpluggablesuperclasses, termmgr/ITTerminalManager2::GetPluggableSuperclasses
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITTerminalManager2::GetPluggableSuperclasses
 - termmgr/ITTerminalManager2::GetPluggableSuperclasses
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Termmgr.h
api_name:
 - ITTerminalManager2.GetPluggableSuperclasses
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

<a href="/windows/desktop/api/termmgr/nn-termmgr-itterminalmanager2">ITTerminalManager2</a>