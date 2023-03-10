---
UID: NF:tapi3if.ITTerminalSupport2.get_PluggableSuperclasses
title: ITTerminalSupport2::get_PluggableSuperclasses (tapi3if.h)
description: The get_PluggableSuperclasses method returns a collection of ITPluggableTerminalSuperclassInfo superclass information interface pointers.
helpviewer_keywords: ["ITTerminalSupport2 interface [TAPI 2.2]","get_PluggableSuperclasses method","ITTerminalSupport2.get_PluggableSuperclasses","ITTerminalSupport2::get_PluggableSuperclasses","_tapi3_itterminalsupport2_get_pluggablesuperclasses","get_PluggableSuperclasses","get_PluggableSuperclasses method [TAPI 2.2]","get_PluggableSuperclasses method [TAPI 2.2]","ITTerminalSupport2 interface","tapi3.itterminalsupport2_get_pluggablesuperclasses","tapi3if/ITTerminalSupport2::get_PluggableSuperclasses"]
old-location: tapi3\itterminalsupport2_get_pluggablesuperclasses.htm
tech.root: tapi3
ms.assetid: 6d66aeca-5ac2-4019-b326-71c3bfb6d28e
ms.date: 12/05/2018
ms.keywords: ITTerminalSupport2 interface [TAPI 2.2],get_PluggableSuperclasses method, ITTerminalSupport2.get_PluggableSuperclasses, ITTerminalSupport2::get_PluggableSuperclasses, _tapi3_itterminalsupport2_get_pluggablesuperclasses, get_PluggableSuperclasses, get_PluggableSuperclasses method [TAPI 2.2], get_PluggableSuperclasses method [TAPI 2.2],ITTerminalSupport2 interface, tapi3.itterminalsupport2_get_pluggablesuperclasses, tapi3if/ITTerminalSupport2::get_PluggableSuperclasses
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
 - ITTerminalSupport2::get_PluggableSuperclasses
 - tapi3if/ITTerminalSupport2::get_PluggableSuperclasses
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
 - ITTerminalSupport2.get_PluggableSuperclasses
---

# ITTerminalSupport2::get_PluggableSuperclasses


## -description

The 
<b>get_PluggableSuperclasses</b> method returns a collection of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo">ITPluggableTerminalSuperclassInfo</a> superclass information interface pointers.

This method is intended for Visual Basic and scripting applications. C/C++ applications can use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport2-enumeratepluggablesuperclasses">EnumeratePluggableSuperclasses</a> method.

## -parameters

### -param pVariant [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo">ITPluggableTerminalSuperclassInfo</a> interface pointers.

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
The <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo">ITPluggableTerminalSuperclassInfo</a> interface returned by <b>ITTerminalSupport2::get_PluggableSuperclasses</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo">ITPluggableTerminalSuperclassInfo</a> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo">ITPluggableTerminalSuperclassInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2">ITTerminalSupport2</a>