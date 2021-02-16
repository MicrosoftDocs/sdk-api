---
UID: NF:termmgr.ITTerminalManager2.GetPluggableTerminalClasses
title: ITTerminalManager2::GetPluggableTerminalClasses (termmgr.h)
description: The GetPluggableTerminalClasses method lists the terminal classes for all pluggable terminals registered under a terminal superclass.
helpviewer_keywords: ["GetPluggableTerminalClasses","GetPluggableTerminalClasses method [TAPI 2.2]","GetPluggableTerminalClasses method [TAPI 2.2]","ITTerminalManager2 interface","ITTerminalManager2 interface [TAPI 2.2]","GetPluggableTerminalClasses method","ITTerminalManager2.GetPluggableTerminalClasses","ITTerminalManager2::GetPluggableTerminalClasses","_tapi3_itterminalmanager2_getpluggableterminalclasses","tapi3.itterminalmanager2_getpluggableterminalclasses","termmgr/ITTerminalManager2::GetPluggableTerminalClasses"]
old-location: tapi3\itterminalmanager2_getpluggableterminalclasses.htm
tech.root: tapi3
ms.assetid: 7f967958-fc32-4336-aae5-bea180ba86d1
ms.date: 12/05/2018
ms.keywords: GetPluggableTerminalClasses, GetPluggableTerminalClasses method [TAPI 2.2], GetPluggableTerminalClasses method [TAPI 2.2],ITTerminalManager2 interface, ITTerminalManager2 interface [TAPI 2.2],GetPluggableTerminalClasses method, ITTerminalManager2.GetPluggableTerminalClasses, ITTerminalManager2::GetPluggableTerminalClasses, _tapi3_itterminalmanager2_getpluggableterminalclasses, tapi3.itterminalmanager2_getpluggableterminalclasses, termmgr/ITTerminalManager2::GetPluggableTerminalClasses
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
 - ITTerminalManager2::GetPluggableTerminalClasses
 - termmgr/ITTerminalManager2::GetPluggableTerminalClasses
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
 - ITTerminalManager2.GetPluggableTerminalClasses
---

# ITTerminalManager2::GetPluggableTerminalClasses


## -description

The 
<b>GetPluggableTerminalClasses</b> method lists the terminal classes for all pluggable terminals registered under a terminal superclass.

## -parameters

### -param iidSuperclass [in]

A <b>BSTR</b> that represents the CLSID for the parent superclass.

### -param dwMediaTypes [in]

Bitwise ORed list of 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media types</a>. The method returns only terminals that support these media types.

### -param pdwNumClasses [in, out]

If the <i>pTerminalClasses</i> parameter is <b>NULL</b>, this parameter returns the total number of terminals registered under the terminal superclass specified by the <i>iidSuperclass</i> parameter. 




If <i>pTerminalClasses</i> is not <b>NULL</b>, and the method completes successfully, this parameter returns a count of the number of terminal IIDs returned in the <i>pTerminalClasses</i> buffer.

### -param pTerminalClasses [out]

Pointer to the buffer to receive the terminals IIDs. This parameter can also be <b>NULL</b>. For more information, see the description of the <i>pdwNumClasses</i> parameter.

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
The <i>pTerminalClasses</i> parameter doesn't represent an IID or list of IIDs.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pTerminalClasses</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itterminalmanager2">ITTerminalManager2</a>