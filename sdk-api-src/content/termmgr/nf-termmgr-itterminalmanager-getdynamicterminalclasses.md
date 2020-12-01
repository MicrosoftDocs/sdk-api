---
UID: NF:termmgr.ITTerminalManager.GetDynamicTerminalClasses
title: ITTerminalManager::GetDynamicTerminalClasses (termmgr.h)
description: The GetDynamicTerminalClasses method gets a list of terminal classes for a set of media types.
helpviewer_keywords: ["GetDynamicTerminalClasses","GetDynamicTerminalClasses method [TAPI 2.2]","GetDynamicTerminalClasses method [TAPI 2.2]","ITTerminalManager interface","ITTerminalManager interface [TAPI 2.2]","GetDynamicTerminalClasses method","ITTerminalManager.GetDynamicTerminalClasses","ITTerminalManager::GetDynamicTerminalClasses","_tapi3_itterminalmanager_getdynamicterminalclasses","tapi3.itterminalmanager_getdynamicterminalclasses","termmgr/ITTerminalManager::GetDynamicTerminalClasses"]
old-location: tapi3\itterminalmanager_getdynamicterminalclasses.htm
tech.root: tapi3
ms.assetid: 6e0ae94c-eab9-4ca2-a982-a5673f73130e
ms.date: 12/05/2018
ms.keywords: GetDynamicTerminalClasses, GetDynamicTerminalClasses method [TAPI 2.2], GetDynamicTerminalClasses method [TAPI 2.2],ITTerminalManager interface, ITTerminalManager interface [TAPI 2.2],GetDynamicTerminalClasses method, ITTerminalManager.GetDynamicTerminalClasses, ITTerminalManager::GetDynamicTerminalClasses, _tapi3_itterminalmanager_getdynamicterminalclasses, tapi3.itterminalmanager_getdynamicterminalclasses, termmgr/ITTerminalManager::GetDynamicTerminalClasses
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
 - ITTerminalManager::GetDynamicTerminalClasses
 - termmgr/ITTerminalManager::GetDynamicTerminalClasses
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
 - ITTerminalManager.GetDynamicTerminalClasses
---

# ITTerminalManager::GetDynamicTerminalClasses


## -description

The 
<b>GetDynamicTerminalClasses</b> method gets a list of terminal classes for a set of media types.

## -parameters

### -param dwMediaTypes [in]

Pointer to 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media types</a>.

### -param pdwNumClasses [in, out]

Number of terminal classes returned.

### -param pTerminalClasses [out]

Pointer to list of 
<a href="/windows/desktop/Tapi/terminal-class">terminal classes</a>.

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

<a href="/windows/desktop/api/termmgr/nn-termmgr-itterminalmanager">ITTerminalManager</a>