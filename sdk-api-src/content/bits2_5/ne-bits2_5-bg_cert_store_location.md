---
UID: NE:bits2_5.BG_CERT_STORE_LOCATION
title: BG_CERT_STORE_LOCATION (bits2_5.h)
description: Defines constants that specify the location of the certificate store.
helpviewer_keywords: ["BG_CERT_STORE_LOCATION","BG_CERT_STORE_LOCATION enumeration [BITS]","BG_CERT_STORE_LOCATION_CURRENT_SERVICE","BG_CERT_STORE_LOCATION_CURRENT_USER","BG_CERT_STORE_LOCATION_CURRENT_USER_GROUP_POLICY","BG_CERT_STORE_LOCATION_LOCAL_MACHINE","BG_CERT_STORE_LOCATION_LOCAL_MACHINE_ENTERPRISE","BG_CERT_STORE_LOCATION_LOCAL_MACHINE_GROUP_POLICY","BG_CERT_STORE_LOCATION_SERVICES","BG_CERT_STORE_LOCATION_USERS","bits.bg_cert_store_location","bits2_5/BG_CERT_STORE_LOCATION","bits2_5/BG_CERT_STORE_LOCATION_CURRENT_SERVICE","bits2_5/BG_CERT_STORE_LOCATION_CURRENT_USER","bits2_5/BG_CERT_STORE_LOCATION_CURRENT_USER_GROUP_POLICY","bits2_5/BG_CERT_STORE_LOCATION_LOCAL_MACHINE","bits2_5/BG_CERT_STORE_LOCATION_LOCAL_MACHINE_ENTERPRISE","bits2_5/BG_CERT_STORE_LOCATION_LOCAL_MACHINE_GROUP_POLICY","bits2_5/BG_CERT_STORE_LOCATION_SERVICES","bits2_5/BG_CERT_STORE_LOCATION_USERS"]
old-location: bits\bg_cert_store_location.htm
tech.root: Bits
ms.assetid: 596b1ba1-6652-4c97-a44d-e8271471d864
ms.date: 02/20/2019
ms.keywords: BG_CERT_STORE_LOCATION, BG_CERT_STORE_LOCATION enumeration [BITS], BG_CERT_STORE_LOCATION_CURRENT_SERVICE, BG_CERT_STORE_LOCATION_CURRENT_USER, BG_CERT_STORE_LOCATION_CURRENT_USER_GROUP_POLICY, BG_CERT_STORE_LOCATION_LOCAL_MACHINE, BG_CERT_STORE_LOCATION_LOCAL_MACHINE_ENTERPRISE, BG_CERT_STORE_LOCATION_LOCAL_MACHINE_GROUP_POLICY, BG_CERT_STORE_LOCATION_SERVICES, BG_CERT_STORE_LOCATION_USERS, bits.bg_cert_store_location, bits2_5/BG_CERT_STORE_LOCATION, bits2_5/BG_CERT_STORE_LOCATION_CURRENT_SERVICE, bits2_5/BG_CERT_STORE_LOCATION_CURRENT_USER, bits2_5/BG_CERT_STORE_LOCATION_CURRENT_USER_GROUP_POLICY, bits2_5/BG_CERT_STORE_LOCATION_LOCAL_MACHINE, bits2_5/BG_CERT_STORE_LOCATION_LOCAL_MACHINE_ENTERPRISE, bits2_5/BG_CERT_STORE_LOCATION_LOCAL_MACHINE_GROUP_POLICY, bits2_5/BG_CERT_STORE_LOCATION_SERVICES, bits2_5/BG_CERT_STORE_LOCATION_USERS
req.header: bits2_5.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits2_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BG_CERT_STORE_LOCATION
req.redist: 
f1_keywords:
 - BG_CERT_STORE_LOCATION
 - bits2_5/BG_CERT_STORE_LOCATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits2_5.h
api_name:
 - BG_CERT_STORE_LOCATION
---

# BG_CERT_STORE_LOCATION enumeration


## -description

Defines constants that specify the location of the certificate store.

## -enum-fields

### -field BG_CERT_STORE_LOCATION_CURRENT_USER:0

Use the current user's certificate store.

### -field BG_CERT_STORE_LOCATION_LOCAL_MACHINE

Use the local computer's certificate store.

### -field BG_CERT_STORE_LOCATION_CURRENT_SERVICE

Use the current service's certificate store.

### -field BG_CERT_STORE_LOCATION_SERVICES

Use a specific service's certificate store.

### -field BG_CERT_STORE_LOCATION_USERS

Use a specific user's certificate store.

### -field BG_CERT_STORE_LOCATION_CURRENT_USER_GROUP_POLICY

Use the current user's group policy certificate store. In a network setting, stores in this location are downloaded to the client computer from the Group Policy Template (GPT) during computer startup, or user logon.

### -field BG_CERT_STORE_LOCATION_LOCAL_MACHINE_GROUP_POLICY

Use the local computer's certificate store. In a network setting, stores in this location are downloaded to the client computer from the Group Policy Template (GPT) during computer startup, or user logon.

### -field BG_CERT_STORE_LOCATION_LOCAL_MACHINE_ENTERPRISE

Use the enterprise certificate store. The enterprise store is shared across domains in the enterprise, and downloaded from the global enterprise directory.

## -remarks

For more information, see [System store locations](/windows/desktop/SecCrypto/system-store-locations).

## -see-also

* [IBackgroundCopyJobHttpOptions::GetClientCertificate method](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-getclientcertificate)
* [IBackgroundCopyJobHttpOptions::SetClientCertificateByID method](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid)
* [IBackgroundCopyJobHttpOptions::SetClientCertificateByName method](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname)

