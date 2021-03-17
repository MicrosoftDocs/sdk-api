---
UID: NF:tapi3if.ITTerminalSupport2.get_PluggableTerminalClasses
title: ITTerminalSupport2::get_PluggableTerminalClasses (tapi3if.h)
description: The get_PluggableTerminalClasses method returns a collection of ITPluggableTerminalClassInfo terminal class information interface pointers.
helpviewer_keywords: ["ITTerminalSupport2 interface [TAPI 2.2]","get_PluggableTerminalClasses method","ITTerminalSupport2.get_PluggableTerminalClasses","ITTerminalSupport2::get_PluggableTerminalClasses","_tapi3_itterminalsupport2_get_pluggableterminalclasses","get_PluggableTerminalClasses","get_PluggableTerminalClasses method [TAPI 2.2]","get_PluggableTerminalClasses method [TAPI 2.2]","ITTerminalSupport2 interface","tapi3.itterminalsupport2_get_pluggableterminalclasses","tapi3if/ITTerminalSupport2::get_PluggableTerminalClasses"]
old-location: tapi3\itterminalsupport2_get_pluggableterminalclasses.htm
tech.root: tapi3
ms.assetid: 4bbb7f77-fc67-4b6b-88fa-2dc5bcfb6c48
ms.date: 12/05/2018
ms.keywords: ITTerminalSupport2 interface [TAPI 2.2],get_PluggableTerminalClasses method, ITTerminalSupport2.get_PluggableTerminalClasses, ITTerminalSupport2::get_PluggableTerminalClasses, _tapi3_itterminalsupport2_get_pluggableterminalclasses, get_PluggableTerminalClasses, get_PluggableTerminalClasses method [TAPI 2.2], get_PluggableTerminalClasses method [TAPI 2.2],ITTerminalSupport2 interface, tapi3.itterminalsupport2_get_pluggableterminalclasses, tapi3if/ITTerminalSupport2::get_PluggableTerminalClasses
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
 - ITTerminalSupport2::get_PluggableTerminalClasses
 - tapi3if/ITTerminalSupport2::get_PluggableTerminalClasses
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
 - ITTerminalSupport2.get_PluggableTerminalClasses
---

# ITTerminalSupport2::get_PluggableTerminalClasses


## -description

The 
<b>get_PluggableTerminalClasses</b> method returns a collection of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo">ITPluggableTerminalClassInfo</a> terminal class information interface pointers.

This method is intended for Visual Basic and scripting applications. C/C++ applications can use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport2-enumeratepluggableterminalclasses">EnumeratePluggableTerminalClasses</a> method.

## -parameters

### -param bstrTerminalSuperclass [in]

The <b>BSTR</b> representation of the CLSID for the terminal superclass.

### -param lMediaType [in]

Bitwise ORed list of 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media types</a> supported by the terminal classes.

### -param pVariant [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo">ITPluggableTerminalClassInfo</a> interface pointers.

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
The <i>lMediaType</i> parameter is not valid.

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
The <i>bstrTerminalSuperclass</i> or <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo">ITPluggableTerminalClassInfo</a> interface returned by <b>ITTerminalSupport2::get_PluggableTerminalClasses</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>ITPluggableTerminalClassInfo</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo">ITPluggableTerminalClassInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2">ITTerminalSupport2</a>