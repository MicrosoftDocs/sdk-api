---
UID: NS:eaptypes._EAP_METHOD_TYPE
title: EAP_METHOD_TYPE (eaptypes.h)
description: Contains type, identification, and author information about an EAP method.
helpviewer_keywords: ["EAP_METHOD_TYPE","EAP_METHOD_TYPE structure [EAPHost]","eaphost.eap_method_type","eaptypes/EAP_METHOD_TYPE"]
old-location: eaphost\eap_method_type.htm
tech.root: eaphost
ms.assetid: 47702dd9-d9c2-4dd5-a12d-23a55b031d27
ms.date: 12/05/2018
ms.keywords: EAP_METHOD_TYPE, EAP_METHOD_TYPE structure [EAPHost], eaphost.eap_method_type, eaptypes/EAP_METHOD_TYPE
req.header: eaptypes.h
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
req.typenames: EAP_METHOD_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_METHOD_TYPE
 - eaptypes/_EAP_METHOD_TYPE
 - EAP_METHOD_TYPE
 - eaptypes/EAP_METHOD_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eaptypes.h
api_name:
 - EAP_METHOD_TYPE
---

# EAP_METHOD_TYPE structure


## -description

The <b>EAP_METHOD_TYPE</b> structure contains  type, identification, and author information about an EAP method.

## -struct-fields

### -field eapType

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_type">EAP_TYPE</a> structure that contains the ID for the EAP method as well as specific vendor information.

### -field dwAuthorId

The numeric ID for the author of the EAP method.

## -see-also

[Common EAPHost API Structures](/windows/win32/eaphost/common-eap-host-api-structures)



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_type">EAP_TYPE</a>