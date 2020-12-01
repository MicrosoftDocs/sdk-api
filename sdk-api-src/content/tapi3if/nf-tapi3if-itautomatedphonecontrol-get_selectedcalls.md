---
UID: NF:tapi3if.ITAutomatedPhoneControl.get_SelectedCalls
title: ITAutomatedPhoneControl::get_SelectedCalls (tapi3if.h)
description: The get_SelectedCalls method retrieves a VARIANT containing a pointer to a collection object indicating which calls are currently selected on this phone. See ITAutomatedPhoneControl::SelectCall for more information.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","get_SelectedCalls method","ITAutomatedPhoneControl.get_SelectedCalls","ITAutomatedPhoneControl::get_SelectedCalls","_tapi3_itautomatedphonecontrol_get_selectedcalls","get_SelectedCalls","get_SelectedCalls method [TAPI 2.2]","get_SelectedCalls method [TAPI 2.2]","ITAutomatedPhoneControl interface","tapi3.itautomatedphonecontrol_get_selectedcalls","tapi3if/ITAutomatedPhoneControl::get_SelectedCalls"]
old-location: tapi3\itautomatedphonecontrol_get_selectedcalls.htm
tech.root: tapi3
ms.assetid: 50196789-c243-4279-8748-960898323992
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],get_SelectedCalls method, ITAutomatedPhoneControl.get_SelectedCalls, ITAutomatedPhoneControl::get_SelectedCalls, _tapi3_itautomatedphonecontrol_get_selectedcalls, get_SelectedCalls, get_SelectedCalls method [TAPI 2.2], get_SelectedCalls method [TAPI 2.2],ITAutomatedPhoneControl interface, tapi3.itautomatedphonecontrol_get_selectedcalls, tapi3if/ITAutomatedPhoneControl::get_SelectedCalls
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
 - ITAutomatedPhoneControl::get_SelectedCalls
 - tapi3if/ITAutomatedPhoneControl::get_SelectedCalls
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
 - ITAutomatedPhoneControl.get_SelectedCalls
---

# ITAutomatedPhoneControl::get_SelectedCalls


## -description

The 
<b>get_SelectedCalls</b> method retrieves a VARIANT containing a pointer to a collection object indicating which calls are currently selected on this phone. See 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-selectcall">ITAutomatedPhoneControl::SelectCall</a> for more information.

This method is intended for applications written in Visual Basic, Java, or various scripting languages. C and C++ programmers should use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-enumerateselectedcalls">EnumerateSelectedCalls</a> method instead.

## -parameters

### -param pVariant [out]

Pointer to a VARIANT containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall">IEnumCall</a> interface pointers.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-enumerateselectedcalls">EnumerateSelectedCalls</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall">IEnumCall</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-selectcall">ITAutomatedPhoneControl::SelectCall</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>