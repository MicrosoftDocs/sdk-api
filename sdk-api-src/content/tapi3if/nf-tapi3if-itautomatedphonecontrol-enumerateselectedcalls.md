---
UID: NF:tapi3if.ITAutomatedPhoneControl.EnumerateSelectedCalls
title: ITAutomatedPhoneControl::EnumerateSelectedCalls (tapi3if.h)
description: The EnumerateSelectedCalls method retrieves an enumerator object indicating which calls are currently selected on this phone. See ITAutomatedPhoneControl::SelectCall for more information.
helpviewer_keywords: ["EnumerateSelectedCalls","EnumerateSelectedCalls method [TAPI 2.2]","EnumerateSelectedCalls method [TAPI 2.2]","ITAutomatedPhoneControl interface","ITAutomatedPhoneControl interface [TAPI 2.2]","EnumerateSelectedCalls method","ITAutomatedPhoneControl.EnumerateSelectedCalls","ITAutomatedPhoneControl::EnumerateSelectedCalls","_tapi3_itautomatedphonecontrol_enumerateselectedcalls","tapi3.itautomatedphonecontrol_enumerateselectedcalls","tapi3if/ITAutomatedPhoneControl::EnumerateSelectedCalls"]
old-location: tapi3\itautomatedphonecontrol_enumerateselectedcalls.htm
tech.root: tapi3
ms.assetid: 534d453c-f47c-48e1-af59-bfa452e2d8d8
ms.date: 12/05/2018
ms.keywords: EnumerateSelectedCalls, EnumerateSelectedCalls method [TAPI 2.2], EnumerateSelectedCalls method [TAPI 2.2],ITAutomatedPhoneControl interface, ITAutomatedPhoneControl interface [TAPI 2.2],EnumerateSelectedCalls method, ITAutomatedPhoneControl.EnumerateSelectedCalls, ITAutomatedPhoneControl::EnumerateSelectedCalls, _tapi3_itautomatedphonecontrol_enumerateselectedcalls, tapi3.itautomatedphonecontrol_enumerateselectedcalls, tapi3if/ITAutomatedPhoneControl::EnumerateSelectedCalls
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAutomatedPhoneControl::EnumerateSelectedCalls
 - tapi3if/ITAutomatedPhoneControl::EnumerateSelectedCalls
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
 - ITAutomatedPhoneControl.EnumerateSelectedCalls
---

# ITAutomatedPhoneControl::EnumerateSelectedCalls


## -description

The 
<b>EnumerateSelectedCalls</b> method retrieves an enumerator object indicating which calls are currently selected on this phone. See 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-selectcall">ITAutomatedPhoneControl::SelectCall</a> for more information.

This method is intended for C and C++ programmers. Applications written in Visual Basic, Java, or various scripting languages should use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_selectedcalls">get_SelectedCalls</a> method instead.

## -parameters

### -param ppCallEnum [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall">IEnumCall</a> interface.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall">IEnumCall</a> interface returned by this method. The application must call the <b>Release</b> method on the 
<b>IEnumCall</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-selectcall">ITAutomatedPhoneControl::SelectCall</a>