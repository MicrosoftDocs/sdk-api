---
UID: NF:tapi3if.ITAutomatedPhoneControl.UnselectCall
title: ITAutomatedPhoneControl::UnselectCall (tapi3if.h)
author: windows-sdk-content
description: The UnselectCall method removes the specified call from this phone object, releasing the phone object's reference to the call object.
old-location: tapi3\itautomatedphonecontrol_unselectcall.htm
tech.root: Tapi
ms.assetid: 3c2a9899-add7-4c09-b32e-11061fc2c5a5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],UnselectCall method, ITAutomatedPhoneControl.UnselectCall, ITAutomatedPhoneControl::UnselectCall, UnselectCall, UnselectCall method [TAPI 2.2], UnselectCall method [TAPI 2.2],ITAutomatedPhoneControl interface, _tapi3_itautomatedphonecontrol_unselectcall, tapi3.itautomatedphonecontrol_unselectcall, tapi3if/ITAutomatedPhoneControl::UnselectCall
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAutomatedPhoneControl.UnselectCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAutomatedPhoneControl::UnselectCall


## -description


The 
<b>UnselectCall</b> method removes the specified call from this phone object, releasing the phone object's reference to the call object. The phone object performs no further call control handling on the call object once the call object has been successfully unselected. See 
<a href="https://msdn.microsoft.com/b9e721cb-8f62-420d-bfc1-f8e634f0f2d4">ITAutomatedPhoneControl::SelectCall</a> for more information.


## -parameters




### -param pCall [in]

Pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -see-also




<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a>



<a href="https://msdn.microsoft.com/b9e721cb-8f62-420d-bfc1-f8e634f0f2d4">ITAutomatedPhoneControl::SelectCall</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>
 

 

