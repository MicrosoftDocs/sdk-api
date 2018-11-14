---
UID: NF:tapi3if.ITPhone.Close
title: ITPhone::Close
author: windows-sdk-content
description: The Close method closes this phone device. The phone device remains closed until the application calls the ITPhone::Open method. For more information, see the following Remarks section.
old-location: tapi3\itphone_close.htm
tech.root: tapi
ms.assetid: 1eae1a14-dd5e-4ba9-8e6e-71e9956cb3e3
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Close, Close method [TAPI 2.2], Close method [TAPI 2.2],ITPhone interface, ITPhone interface [TAPI 2.2],Close method, ITPhone.Close, ITPhone::Close, _tapi3_itphone_close, tapi3.itphone_close, tapi3if/ITPhone::Close
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITPhone.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3if.h
: 
- ITPhone.Close
: 
---

# ITPhone::Close


## -description


The 
<b>Close</b> method closes this phone device. The phone device remains closed until the application calls the 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> method. For more information, see the following Remarks section.

This method is analogous to the TAPI 2.<i>x</i>
<a href="https://msdn.microsoft.com/8fba6d5e-0d8c-488f-a17c-4852b487e300">phoneOpen</a> function; please see the TAPI 2.<i>x</i> documentation for more information.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



While a phone is closed, the application does not receive events pertaining to the phone.

A phone must be open with owner privilege for the application to set the state of the phone. Querying the state of the phone can typically be done even if the phone is not open; for more details, see the individual methods of the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface.

After the phone device has been successfully closed, any 
<a href="https://msdn.microsoft.com/60d4f079-75ee-4aeb-9e7c-0b16d90da754">ITAutomatedPhoneControl</a> interface pointer obtained for this phone object is no longer valid.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>
 

 

