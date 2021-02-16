---
UID: NF:tapi3if.ITTerminal.get_Name
title: ITTerminal::get_Name (tapi3if.h)
description: The get_Name method gets a descriptive name of the terminal. The name must be usable to the user.
helpviewer_keywords: ["ITTerminal interface [TAPI 2.2]","get_Name method","ITTerminal.get_Name","ITTerminal::get_Name","_tapi3_itterminal_get_name","get_Name","get_Name method [TAPI 2.2]","get_Name method [TAPI 2.2]","ITTerminal interface","tapi3.itterminal_get_name","tapi3if/ITTerminal::get_Name"]
old-location: tapi3\itterminal_get_name.htm
tech.root: tapi3
ms.assetid: ad3a44ff-ad63-4fd0-9cfd-c97c0cea6162
ms.date: 12/05/2018
ms.keywords: ITTerminal interface [TAPI 2.2],get_Name method, ITTerminal.get_Name, ITTerminal::get_Name, _tapi3_itterminal_get_name, get_Name, get_Name method [TAPI 2.2], get_Name method [TAPI 2.2],ITTerminal interface, tapi3.itterminal_get_name, tapi3if/ITTerminal::get_Name
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITTerminal::get_Name
 - tapi3if/ITTerminal::get_Name
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITTerminal.get_Name
---

# ITTerminal::get_Name


## -description

The 
<b>get_Name</b> method gets a descriptive name of the terminal. The name must be usable to the user.

## -parameters

### -param ppName [out]

Pointer to <b>BSTR</b> containing the name of the terminal.

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
The <i>ppName</i> parameter is not a valid pointer.

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

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppName</i> parameter.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/Tapi/terminal-object-interfaces">Terminal Object Interfaces</a>