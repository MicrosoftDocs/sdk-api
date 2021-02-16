---
UID: NF:tapi3if.ITTerminalSupport.CreateTerminal
title: ITTerminalSupport::CreateTerminal (tapi3if.h)
description: The CreateTerminal method creates and initializes a new ITTerminal object based on the dynamic terminal class and media. The terminal class is identified by a GUID. The GUID must be converted to a string using StringFromIID to pass to this method.
helpviewer_keywords: ["CreateTerminal","CreateTerminal method [TAPI 2.2]","CreateTerminal method [TAPI 2.2]","ITTerminalSupport interface","ITTerminalSupport interface [TAPI 2.2]","CreateTerminal method","ITTerminalSupport.CreateTerminal","ITTerminalSupport::CreateTerminal","_tapi3_itterminalsupport_createterminal","tapi3.itterminalsupport_createterminal","tapi3if/ITTerminalSupport::CreateTerminal"]
old-location: tapi3\itterminalsupport_createterminal.htm
tech.root: tapi3
ms.assetid: 2a2a037a-753c-4dd4-b6ce-10b69f2e2421
ms.date: 12/05/2018
ms.keywords: CreateTerminal, CreateTerminal method [TAPI 2.2], CreateTerminal method [TAPI 2.2],ITTerminalSupport interface, ITTerminalSupport interface [TAPI 2.2],CreateTerminal method, ITTerminalSupport.CreateTerminal, ITTerminalSupport::CreateTerminal, _tapi3_itterminalsupport_createterminal, tapi3.itterminalsupport_createterminal, tapi3if/ITTerminalSupport::CreateTerminal
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
 - ITTerminalSupport::CreateTerminal
 - tapi3if/ITTerminalSupport::CreateTerminal
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
 - ITTerminalSupport.CreateTerminal
---

# ITTerminalSupport::CreateTerminal


## -description

The 
<b>CreateTerminal</b> method creates and initializes a new 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> object based on the dynamic terminal class and media. The 
<a href="/windows/desktop/Tapi/terminal-class">terminal class</a> is identified by a GUID. The GUID must be converted to a string using 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid">StringFromIID</a> to pass to this method.

## -parameters

### -param pTerminalClass [in]

Pointer to <b>BSTR</b> containing the 
<a href="/windows/desktop/Tapi/terminal-class">terminal class</a> (GUID) for the new terminal object.

### -param lMediaType [in]

Pointer to the 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a> for the new terminal object.

### -param Direction [in]

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">TERMINAL_DIRECTION</a> descriptor of the terminal direction.

### -param ppTerminal [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> object created.

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
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> object.

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
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pTerminalClass</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

Once a terminal is created, it can be selected onto only one call.

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<b>ITTerminal</b> interface returned by <b>ITTerminalSupport::CreateTerminal</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>ITTerminal</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport">ITTerminalSupport</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">TERMINAL_DIRECTION</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/Tapi/terminal-object-interfaces">Terminal Object Interfaces</a>



<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a>



<a href="/windows/desktop/Tapi/terminal-class">terminal class</a>