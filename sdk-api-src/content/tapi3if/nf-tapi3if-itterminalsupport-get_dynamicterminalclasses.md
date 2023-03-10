---
UID: NF:tapi3if.ITTerminalSupport.get_DynamicTerminalClasses
title: ITTerminalSupport::get_DynamicTerminalClasses (tapi3if.h)
description: The get_DynamicTerminalClasses method creates a collection of currently available dynamic terminals.
helpviewer_keywords: ["ITTerminalSupport interface [TAPI 2.2]","get_DynamicTerminalClasses method","ITTerminalSupport.get_DynamicTerminalClasses","ITTerminalSupport::get_DynamicTerminalClasses","_tapi3_itterminalsupport_get_dynamicterminalclasses","get_DynamicTerminalClasses","get_DynamicTerminalClasses method [TAPI 2.2]","get_DynamicTerminalClasses method [TAPI 2.2]","ITTerminalSupport interface","tapi3.itterminalsupport_get_dynamicterminalclasses","tapi3if/ITTerminalSupport::get_DynamicTerminalClasses"]
old-location: tapi3\itterminalsupport_get_dynamicterminalclasses.htm
tech.root: tapi3
ms.assetid: 258fad5c-6269-45ab-bdc0-d38338f8e515
ms.date: 12/05/2018
ms.keywords: ITTerminalSupport interface [TAPI 2.2],get_DynamicTerminalClasses method, ITTerminalSupport.get_DynamicTerminalClasses, ITTerminalSupport::get_DynamicTerminalClasses, _tapi3_itterminalsupport_get_dynamicterminalclasses, get_DynamicTerminalClasses, get_DynamicTerminalClasses method [TAPI 2.2], get_DynamicTerminalClasses method [TAPI 2.2],ITTerminalSupport interface, tapi3.itterminalsupport_get_dynamicterminalclasses, tapi3if/ITTerminalSupport::get_DynamicTerminalClasses
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
 - ITTerminalSupport::get_DynamicTerminalClasses
 - tapi3if/ITTerminalSupport::get_DynamicTerminalClasses
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
 - ITTerminalSupport.get_DynamicTerminalClasses
---

# ITTerminalSupport::get_DynamicTerminalClasses


## -description

The 
<b>get_DynamicTerminalClasses</b> method creates a collection of currently available dynamic terminals. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses">EnumerateDynamicTerminalClasses</a> method.

## -parameters

### -param pVariant [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/Tapi/terminal-class">terminal classes</a> in a string (<b>BSTR</b>) format.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

An application calls this method to find out which dynamic terminal classes are supported by this address in a call to 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal">ITTerminalSupport::CreateTerminal</a>.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport">ITTerminalSupport</a>



<a href="/windows/desktop/Tapi/terminal-class">Terminal Class</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/Tapi/terminal-object-interfaces">Terminal Object Interfaces</a>