---
UID: NF:tapi3if.ITTerminalSupport2.EnumeratePluggableTerminalClasses
title: ITTerminalSupport2::EnumeratePluggableTerminalClasses (tapi3if.h)
description: The EnumeratePluggableTerminalClasses method enumerates the pluggable terminal classes registered under a given superclass.
helpviewer_keywords: ["EnumeratePluggableTerminalClasses","EnumeratePluggableTerminalClasses method [TAPI 2.2]","EnumeratePluggableTerminalClasses method [TAPI 2.2]","ITTerminalSupport2 interface","ITTerminalSupport2 interface [TAPI 2.2]","EnumeratePluggableTerminalClasses method","ITTerminalSupport2.EnumeratePluggableTerminalClasses","ITTerminalSupport2::EnumeratePluggableTerminalClasses","_tapi3_itterminalsupport2_enumeratepluggableterminalclasses","tapi3.itterminalsupport2_enumeratepluggableterminalclasses","tapi3if/ITTerminalSupport2::EnumeratePluggableTerminalClasses"]
old-location: tapi3\itterminalsupport2_enumeratepluggableterminalclasses.htm
tech.root: tapi3
ms.assetid: e8a10b1b-b08e-49b2-bfc6-9f8f4dbc1248
ms.date: 12/05/2018
ms.keywords: EnumeratePluggableTerminalClasses, EnumeratePluggableTerminalClasses method [TAPI 2.2], EnumeratePluggableTerminalClasses method [TAPI 2.2],ITTerminalSupport2 interface, ITTerminalSupport2 interface [TAPI 2.2],EnumeratePluggableTerminalClasses method, ITTerminalSupport2.EnumeratePluggableTerminalClasses, ITTerminalSupport2::EnumeratePluggableTerminalClasses, _tapi3_itterminalsupport2_enumeratepluggableterminalclasses, tapi3.itterminalsupport2_enumeratepluggableterminalclasses, tapi3if/ITTerminalSupport2::EnumeratePluggableTerminalClasses
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
 - ITTerminalSupport2::EnumeratePluggableTerminalClasses
 - tapi3if/ITTerminalSupport2::EnumeratePluggableTerminalClasses
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
 - ITTerminalSupport2.EnumeratePluggableTerminalClasses
---

# ITTerminalSupport2::EnumeratePluggableTerminalClasses


## -description

The 
<b>EnumeratePluggableTerminalClasses</b> method enumerates the pluggable terminal classes registered under a given superclass.

This method is intended for C/C++ applications. Visual Basic and scripting applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport2-get_pluggableterminalclasses">get_PluggableTerminalClasses</a> method.

## -parameters

### -param iidTerminalSuperclass [in]

CLSID for the terminal superclass.

### -param lMediaType [in]

Bitwise ORed list of 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media types</a> supported by the terminal classes.

### -param ppClassEnumerator [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggableterminalclassinfo">IEnumPluggableTerminalClassInfo</a> interface.

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
The <i>ppClassEnumerator</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggableterminalclassinfo">IEnumPluggableTerminalClassInfo</a> interface returned by <b>ITTerminalSupport2::EnumeratePluggableTerminalClasses</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>IEnumPluggableTerminalClassInfo</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggableterminalclassinfo">IEnumPluggableTerminalClassInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2">ITTerminalSupport2</a>