---
UID: NF:termmgr.ITPluggableTerminalSuperclassRegistration.EnumerateTerminalClasses
title: ITPluggableTerminalSuperclassRegistration::EnumerateTerminalClasses (termmgr.h)
description: The EnumerateTerminalClasses method lists all terminal classes for the current terminal superclass.
helpviewer_keywords: ["EnumerateTerminalClasses","EnumerateTerminalClasses method [TAPI 2.2]","EnumerateTerminalClasses method [TAPI 2.2]","ITPluggableTerminalSuperclassRegistration interface","ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2]","EnumerateTerminalClasses method","ITPluggableTerminalSuperclassRegistration.EnumerateTerminalClasses","ITPluggableTerminalSuperclassRegistration::EnumerateTerminalClasses","_tapi3_itpluggableterminalsuperclassregistration_enumerateterminalclasses","tapi3.itpluggableterminalsuperclassregistration_enumerateterminalclasses","termmgr/ITPluggableTerminalSuperclassRegistration::EnumerateTerminalClasses"]
old-location: tapi3\itpluggableterminalsuperclassregistration_enumerateterminalclasses.htm
tech.root: tapi3
ms.assetid: dc75972d-7917-406d-8ed8-e05679ab86eb
ms.date: 12/05/2018
ms.keywords: EnumerateTerminalClasses, EnumerateTerminalClasses method [TAPI 2.2], EnumerateTerminalClasses method [TAPI 2.2],ITPluggableTerminalSuperclassRegistration interface, ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2],EnumerateTerminalClasses method, ITPluggableTerminalSuperclassRegistration.EnumerateTerminalClasses, ITPluggableTerminalSuperclassRegistration::EnumerateTerminalClasses, _tapi3_itpluggableterminalsuperclassregistration_enumerateterminalclasses, tapi3.itpluggableterminalsuperclassregistration_enumerateterminalclasses, termmgr/ITPluggableTerminalSuperclassRegistration::EnumerateTerminalClasses
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
 - ITPluggableTerminalSuperclassRegistration::EnumerateTerminalClasses
 - termmgr/ITPluggableTerminalSuperclassRegistration::EnumerateTerminalClasses
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
 - ITPluggableTerminalSuperclassRegistration.EnumerateTerminalClasses
---

# ITPluggableTerminalSuperclassRegistration::EnumerateTerminalClasses


## -description

The 
<b>EnumerateTerminalClasses</b> method lists all terminal classes for the current terminal superclass.

## -parameters

### -param ppTerminals [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass">IEnumTerminalClass</a> interface that enumerates the terminal classes.

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
The <i>ppTerminals</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass">IEnumTerminalClass</a> interface returned by <b>ITPluggableTerminalSuperclassRegistration::EnumerateTerminalClasses</b>. The application must call <b>Release</b> on the 
<b>IEnumTerminalClass</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass">IEnumTerminalClass</a>



<a href="/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalsuperclassregistration">ITPluggableTerminalSuperclassRegistration</a>