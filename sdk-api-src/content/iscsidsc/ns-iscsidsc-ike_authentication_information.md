---
UID: NS:iscsidsc.IKE_AUTHENTICATION_INFORMATION
title: IKE_AUTHENTICATION_INFORMATION (iscsidsc.h)
description: IKE_AUTHENTICATION_INFORMATION structure contains Internet Key Exchange (IKE) authentication information used to establish a secure channel between two key management daemons.
helpviewer_keywords: ["*PIKE_AUTHENTICATION_INFORMATION","IKE_AUTHENTICATION_INFORMATION","IKE_AUTHENTICATION_INFORMATION structure [iSCSI Discovery Library API]","PIKE_AUTHENTICATION_INFORMATION","PIKE_AUTHENTICATION_INFORMATION structure pointer [iSCSI Discovery Library API]","iscsidisc.ike_authentication_information","iscsidsc/IKE_AUTHENTICATION_INFORMATION","iscsidsc/PIKE_AUTHENTICATION_INFORMATION"]
old-location: iscsidisc\ike_authentication_information.htm
tech.root: iSCSIDisc
ms.assetid: d61036f5-a5e8-4c1a-8f99-57fe8e5c5bd0
ms.date: 12/05/2018
ms.keywords: '*PIKE_AUTHENTICATION_INFORMATION, IKE_AUTHENTICATION_INFORMATION, IKE_AUTHENTICATION_INFORMATION structure [iSCSI Discovery Library API], PIKE_AUTHENTICATION_INFORMATION, PIKE_AUTHENTICATION_INFORMATION structure pointer [iSCSI Discovery Library API], iscsidisc.ike_authentication_information, iscsidsc/IKE_AUTHENTICATION_INFORMATION, iscsidsc/PIKE_AUTHENTICATION_INFORMATION'
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
req.typenames: IKE_AUTHENTICATION_INFORMATION, *PIKE_AUTHENTICATION_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PIKE_AUTHENTICATION_INFORMATION
 - iscsidsc/PIKE_AUTHENTICATION_INFORMATION
 - IKE_AUTHENTICATION_INFORMATION
 - iscsidsc/IKE_AUTHENTICATION_INFORMATION
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
 - IKE_AUTHENTICATION_INFORMATION
---

# IKE_AUTHENTICATION_INFORMATION structure


## -description

The <b>IKE_AUTHENTICATION_INFORMATION</b> structure contains Internet Key Exchange (IKE) authentication information used to establish a secure channel between two key management daemons.

## -struct-fields

### -field AuthMethod

A <a href="/previous-versions/windows/desktop/api/iscsidsc/ne-iscsidsc-ike_authentication_method">IKE_AUTHENTICATION_METHOD</a> structure that indicates the authentication method.

### -field PsKey

A <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-ike_authentication_preshared_key">IKE_AUTHENTICATION_PRESHARED_KEY</a> structure that contains the preshared key that establishes a secure channel between two key management daemons.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/ne-iscsidsc-ike_authentication_method">IKE_AUTHENTICATION_METHOD</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-ike_authentication_preshared_key">IKE_AUTHENTICATION_PRESHARED_KEY</a>

