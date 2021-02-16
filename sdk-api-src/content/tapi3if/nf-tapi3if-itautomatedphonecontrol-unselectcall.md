---
UID: NF:tapi3if.ITAutomatedPhoneControl.UnselectCall
title: ITAutomatedPhoneControl::UnselectCall (tapi3if.h)
description: The UnselectCall method removes the specified call from this phone object, releasing the phone object's reference to the call object.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","UnselectCall method","ITAutomatedPhoneControl.UnselectCall","ITAutomatedPhoneControl::UnselectCall","UnselectCall","UnselectCall method [TAPI 2.2]","UnselectCall method [TAPI 2.2]","ITAutomatedPhoneControl interface","_tapi3_itautomatedphonecontrol_unselectcall","tapi3.itautomatedphonecontrol_unselectcall","tapi3if/ITAutomatedPhoneControl::UnselectCall"]
old-location: tapi3\itautomatedphonecontrol_unselectcall.htm
tech.root: tapi3
ms.assetid: 3c2a9899-add7-4c09-b32e-11061fc2c5a5
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],UnselectCall method, ITAutomatedPhoneControl.UnselectCall, ITAutomatedPhoneControl::UnselectCall, UnselectCall, UnselectCall method [TAPI 2.2], UnselectCall method [TAPI 2.2],ITAutomatedPhoneControl interface, _tapi3_itautomatedphonecontrol_unselectcall, tapi3.itautomatedphonecontrol_unselectcall, tapi3if/ITAutomatedPhoneControl::UnselectCall
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
 - ITAutomatedPhoneControl::UnselectCall
 - tapi3if/ITAutomatedPhoneControl::UnselectCall
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
 - ITAutomatedPhoneControl.UnselectCall
---

# ITAutomatedPhoneControl::UnselectCall


## -description

The 
<b>UnselectCall</b> method removes the specified call from this phone object, releasing the phone object's reference to the call object. The phone object performs no further call control handling on the call object once the call object has been successfully unselected. See 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-selectcall">ITAutomatedPhoneControl::SelectCall</a> for more information.

## -parameters

### -param pCall [in]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-selectcall">ITAutomatedPhoneControl::SelectCall</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>