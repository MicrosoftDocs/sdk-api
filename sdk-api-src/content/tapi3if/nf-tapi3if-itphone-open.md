---
UID: NF:tapi3if.ITPhone.Open
title: ITPhone::Open
author: windows-sdk-content
description: The Open method opens this phone device. The phone device remains open until the application calls ITPhone::Close or until TAPI is shut down.
old-location: tapi3\itphone_open.htm
tech.root: TAPI
ms.assetid: d9efe2f7-3628-4e1f-b554-a6889d82a973
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITPhone interface [TAPI 2.2],Open method, ITPhone.Open, ITPhone::Open, Open, Open method [TAPI 2.2], Open method [TAPI 2.2],ITPhone interface, _tapi3_itphone_open, tapi3.itphone_open, tapi3if/ITPhone::Open
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
 - ITPhone.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPhone::Open


## -description


The 
<b>Open</b> method opens this phone device. The phone device remains open until the application calls 
<a href="https://msdn.microsoft.com/1eae1a14-dd5e-4ba9-8e6e-71e9956cb3e3">ITPhone::Close</a> or until TAPI is shut down.

This method is analogous to the TAPI 2.<i>x</i>
<a href="https://msdn.microsoft.com/8fba6d5e-0d8c-488f-a17c-4852b487e300">phoneOpen</a> function; please see the TAPI 2.<i>x</i> documentation for more information.


## -parameters




### -param Privilege [in]

The 
<a href="https://msdn.microsoft.com/f1c162c6-058d-4cf2-a493-17b7752ffeeb">PHONE_PRIVILEGE</a> descriptor for the application's privilege status with respect to the phone device.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



While a phone is open, the application receives events pertaining to the phone.

Also, a phone must be open with owner privilege for the application to set the state of the phone. Querying the state of the phone can typically be done even if the phone is not open; for more details, see the individual methods of the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>
 

 

