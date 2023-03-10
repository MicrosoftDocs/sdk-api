---
UID: NF:termmgr.ITPluggableTerminalSuperclassRegistration.get_TerminalClasses
title: ITPluggableTerminalSuperclassRegistration::get_TerminalClasses (termmgr.h)
description: The get_TerminalClasses method gets the terminal classes for this pluggable terminal superclass.
helpviewer_keywords: ["ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2]","get_TerminalClasses method","ITPluggableTerminalSuperclassRegistration.get_TerminalClasses","ITPluggableTerminalSuperclassRegistration::get_TerminalClasses","_tapi3_itpluggableterminalsuperclassregistration_get_terminalclasses","get_TerminalClasses","get_TerminalClasses method [TAPI 2.2]","get_TerminalClasses method [TAPI 2.2]","ITPluggableTerminalSuperclassRegistration interface","tapi3.itpluggableterminalsuperclassregistration_get_terminalclasses","termmgr/ITPluggableTerminalSuperclassRegistration::get_TerminalClasses"]
old-location: tapi3\itpluggableterminalsuperclassregistration_get_terminalclasses.htm
tech.root: tapi3
ms.assetid: 414ce7fe-e664-4915-84d6-0d4b6c750cf3
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2],get_TerminalClasses method, ITPluggableTerminalSuperclassRegistration.get_TerminalClasses, ITPluggableTerminalSuperclassRegistration::get_TerminalClasses, _tapi3_itpluggableterminalsuperclassregistration_get_terminalclasses, get_TerminalClasses, get_TerminalClasses method [TAPI 2.2], get_TerminalClasses method [TAPI 2.2],ITPluggableTerminalSuperclassRegistration interface, tapi3.itpluggableterminalsuperclassregistration_get_terminalclasses, termmgr/ITPluggableTerminalSuperclassRegistration::get_TerminalClasses
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITPluggableTerminalSuperclassRegistration::get_TerminalClasses
 - termmgr/ITPluggableTerminalSuperclassRegistration::get_TerminalClasses
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPluggableTerminalSuperclassRegistration.get_TerminalClasses
---

# ITPluggableTerminalSuperclassRegistration::get_TerminalClasses


## -description

The 
<b>get_TerminalClasses</b> method gets the terminal classes for this pluggable terminal superclass.

## -parameters

### -param pTerminals [out]

 Pointer to a <b>VARIANT</b> containing a <b>SAFEARRAY</b> of <b>BSTR</b> strings. Each string represents a terminal class.

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
The <i>pTerminals</i> parameter is not valid.

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

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalsuperclassregistration">ITPluggableTerminalSuperclassRegistration</a>