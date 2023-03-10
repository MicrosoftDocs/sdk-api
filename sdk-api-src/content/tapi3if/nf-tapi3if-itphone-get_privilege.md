---
UID: NF:tapi3if.ITPhone.get_Privilege
title: ITPhone::get_Privilege (tapi3if.h)
description: The get_Privilege method retrieves the privilege of the open phone.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","get_Privilege method","ITPhone.get_Privilege","ITPhone::get_Privilege","_tapi3_itphone_get_privilege","get_Privilege","get_Privilege method [TAPI 2.2]","get_Privilege method [TAPI 2.2]","ITPhone interface","tapi3.itphone_get_privilege","tapi3if/ITPhone::get_Privilege"]
old-location: tapi3\itphone_get_privilege.htm
tech.root: tapi3
ms.assetid: 88103a48-a5cd-43a7-a88e-9b16313b35c2
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_Privilege method, ITPhone.get_Privilege, ITPhone::get_Privilege, _tapi3_itphone_get_privilege, get_Privilege, get_Privilege method [TAPI 2.2], get_Privilege method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_privilege, tapi3if/ITPhone::get_Privilege
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
 - ITPhone::get_Privilege
 - tapi3if/ITPhone::get_Privilege
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
 - ITPhone.get_Privilege
---

# ITPhone::get_Privilege


## -description

The 
<b>get_Privilege</b> method retrieves the privilege of the open phone.

The application must call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before invoking this method; otherwise, the invocation fails.

## -parameters

### -param pPrivilege [out]

The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_privilege">PHONE_PRIVILEGE</a> descriptor for the application's privilege status with respect to the phone device.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>