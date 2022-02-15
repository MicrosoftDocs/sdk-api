---
UID: NE:iscsidsc.__unnamed_enum_2
title: IKE_AUTHENTICATION_METHOD (iscsidsc.h)
description: IKE_AUTHENTICATION_METHOD enumeration indicates the type of Internet Key Exchange (IKE) authentication method.
helpviewer_keywords: ["*PIKE_AUTHENTICATION_METHOD","IKE_AUTHENTICATION_METHOD","IKE_AUTHENTICATION_METHOD enumeration [iSCSI Discovery Library API]","IKE_AUTHENTICATION_PRESHARED_KEY_METHOD","PIKE_AUTHENTICATION_METHOD","PIKE_AUTHENTICATION_METHOD enumeration pointer [iSCSI Discovery Library API]","iscsidisc.ike_authentication_method","iscsidsc/IKE_AUTHENTICATION_METHOD","iscsidsc/IKE_AUTHENTICATION_PRESHARED_KEY_METHOD","iscsidsc/PIKE_AUTHENTICATION_METHOD"]
old-location: iscsidisc\ike_authentication_method.htm
tech.root: iSCSIDisc
ms.assetid: be92f3db-93c5-41e3-bd5a-f929f911da39
ms.date: 12/05/2018
ms.keywords: '*PIKE_AUTHENTICATION_METHOD, IKE_AUTHENTICATION_METHOD, IKE_AUTHENTICATION_METHOD enumeration [iSCSI Discovery Library API], IKE_AUTHENTICATION_PRESHARED_KEY_METHOD, PIKE_AUTHENTICATION_METHOD, PIKE_AUTHENTICATION_METHOD enumeration pointer [iSCSI Discovery Library API], iscsidisc.ike_authentication_method, iscsidsc/IKE_AUTHENTICATION_METHOD, iscsidsc/IKE_AUTHENTICATION_PRESHARED_KEY_METHOD, iscsidsc/PIKE_AUTHENTICATION_METHOD'
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: IKE_AUTHENTICATION_METHOD, *PIKE_AUTHENTICATION_METHOD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PIKE_AUTHENTICATION_METHOD
 - iscsidsc/PIKE_AUTHENTICATION_METHOD
 - IKE_AUTHENTICATION_METHOD
 - iscsidsc/IKE_AUTHENTICATION_METHOD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iscsidsc.h
api_name:
 - IKE_AUTHENTICATION_METHOD
---

# IKE_AUTHENTICATION_METHOD enumeration


## -description

The <b>IKE_AUTHENTICATION_METHOD</b> enumeration indicates the type of Internet Key Exchange (IKE) authentication method.

## -enum-fields

### -field IKE_AUTHENTICATION_PRESHARED_KEY_METHOD:1

The authentication method was preshared.

## -remarks

Used in conjunction with the <a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-setiscsiikeinfoa">SetIScsiIKEInfo</a> function to establish the IPsec policy to use during iSCSI operations.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-ike_authentication_information">IKE_AUTHENTICATION_INFORMATION</a>
