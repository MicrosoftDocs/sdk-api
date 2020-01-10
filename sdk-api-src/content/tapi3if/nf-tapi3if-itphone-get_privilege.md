---
UID: NF:tapi3if.ITPhone.get_Privilege
title: ITPhone::get_Privilege (tapi3if.h)
description: The get_Privilege method retrieves the privilege of the open phone.
old-location: tapi3\itphone_get_privilege.htm
tech.root: Tapi
ms.assetid: 88103a48-a5cd-43a7-a88e-9b16313b35c2
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_Privilege method, ITPhone.get_Privilege, ITPhone::get_Privilege, _tapi3_itphone_get_privilege, get_Privilege, get_Privilege method [TAPI 2.2], get_Privilege method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_privilege, tapi3if/ITPhone::get_Privilege
f1_keywords:
- tapi3if/ITPhone.get_Privilege
dev_langs:
- c++
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
- ITPhone.get_Privilege
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPhone::get_Privilege


## -description


The 
<b>get_Privilege</b> method retrieves the privilege of the open phone.

The application must call 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before invoking this method; otherwise, the invocation fails.


## -parameters




### -param pPrivilege [out]

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-phone_privilege">PHONE_PRIVILEGE</a> descriptor for the application's privilege status with respect to the phone device.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>
 

 

