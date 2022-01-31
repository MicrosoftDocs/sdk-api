---
UID: NE:tapi3if.PHONE_PRIVILEGE
title: PHONE_PRIVILEGE (tapi3if.h)
description: The PHONE_PRIVILEGE enum indicates the application's privilege status with respect to the current phone device.
helpviewer_keywords: ["PHONE_PRIVILEGE","PHONE_PRIVILEGE enumeration [TAPI 2.2]","PP_MONITOR","PP_OWNER","_tapi3_phone_privilege","tapi3.phone_privilege","tapi3if/PHONE_PRIVILEGE","tapi3if/PP_MONITOR","tapi3if/PP_OWNER"]
old-location: tapi3\phone_privilege.htm
tech.root: tapi3
ms.assetid: f1c162c6-058d-4cf2-a493-17b7752ffeeb
ms.date: 12/05/2018
ms.keywords: PHONE_PRIVILEGE, PHONE_PRIVILEGE enumeration [TAPI 2.2], PP_MONITOR, PP_OWNER, _tapi3_phone_privilege, tapi3.phone_privilege, tapi3if/PHONE_PRIVILEGE, tapi3if/PP_MONITOR, tapi3if/PP_OWNER
req.header: tapi3if.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PHONE_PRIVILEGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PHONE_PRIVILEGE
 - tapi3if/PHONE_PRIVILEGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - PHONE_PRIVILEGE
---

# PHONE_PRIVILEGE enumeration


## -description

The 
<b>PHONE_PRIVILEGE</b> enum indicates the application's privilege status with respect to the current phone device.

## -enum-fields

### -field PP_OWNER:0

The application has owner privileges for the current phone session.

### -field PP_MONITOR

The application has monitor privileges for the current phone session.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_privilege">ITPhone::get_Privilege</a>
