---
UID: NE:ntdsapi.__unnamed_enum_3
title: DS_SPN_NAME_TYPE (ntdsapi.h)
description: The DS_SPN_NAME_TYPE enumeration is used by the DsGetSPN function to identify the format for composing SPNs.
helpviewer_keywords: ["DS_SPN_DNS_HOST","DS_SPN_DN_HOST","DS_SPN_DOMAIN","DS_SPN_NAME_TYPE","DS_SPN_NAME_TYPE enumeration [Active Directory]","DS_SPN_NB_DOMAIN","DS_SPN_NB_HOST","DS_SPN_SERVICE","_glines_ds_spn_name_type","ad.ds__spn__name__type","ad.ds_spn_name_type","ntdsapi/DS_SPN_DNS_HOST","ntdsapi/DS_SPN_DN_HOST","ntdsapi/DS_SPN_DOMAIN","ntdsapi/DS_SPN_NAME_TYPE","ntdsapi/DS_SPN_NB_DOMAIN","ntdsapi/DS_SPN_NB_HOST","ntdsapi/DS_SPN_SERVICE"]
old-location: ad\ds_spn_name_type.htm
tech.root: ad
ms.assetid: 7aab22a6-1fe1-4127-97d3-54287d770790
ms.date: 12/05/2018
ms.keywords: DS_SPN_DNS_HOST, DS_SPN_DN_HOST, DS_SPN_DOMAIN, DS_SPN_NAME_TYPE, DS_SPN_NAME_TYPE enumeration [Active Directory], DS_SPN_NB_DOMAIN, DS_SPN_NB_HOST, DS_SPN_SERVICE, _glines_ds_spn_name_type, ad.ds__spn__name__type, ad.ds_spn_name_type, ntdsapi/DS_SPN_DNS_HOST, ntdsapi/DS_SPN_DN_HOST, ntdsapi/DS_SPN_DOMAIN, ntdsapi/DS_SPN_NAME_TYPE, ntdsapi/DS_SPN_NB_DOMAIN, ntdsapi/DS_SPN_NB_HOST, ntdsapi/DS_SPN_SERVICE
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: DS_SPN_NAME_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DS_SPN_NAME_TYPE
 - ntdsapi/DS_SPN_NAME_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_SPN_NAME_TYPE
---

# DS_SPN_NAME_TYPE enumeration


## -description

The <b>DS_SPN_NAME_TYPE</b> enumeration is used by the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetspna">DsGetSPN</a> function to identify the format for composing SPNs.

## -enum-fields

### -field DS_SPN_DNS_HOST:0

The SPN format for the distinguished name service of the host-based service, which provides services identified with its host computer. This SPN uses the following format:


```cpp
jeffsmith.fabrikam.com
```

### -field DS_SPN_DN_HOST:1

The SPN format for the distinguished name of the host-based service, which provides services identified with its host computer. This SPN uses the following format:


```cpp
cn=jeffsmith,ou=computers,dc=fabrikam,dc=com
```

### -field DS_SPN_NB_HOST:2

The SPN format for the NetBIOS service of the host-based service, which provides services identified with its host computer. This SPN uses the following format:


```cpp
jeffsmith-nec
```

### -field DS_SPN_DOMAIN:3

The SPN format for a replicable service that provides services to the specified domain. This SPN uses the following format:


```cpp
fabrikam.com
```

### -field DS_SPN_NB_DOMAIN:4

The SPN format for a replicable service that provides services to the specified NetBIOS domain. This SPN uses the following format:


```cpp
fabrikam
```

### -field DS_SPN_SERVICE:5

The SPN format for a specified service. This SPN uses the following formats, depending on which service is used:


```cpp
cn=anRpcService,cn=RPC Services,cn=system,dc=fabrikam,dc=com
```



```cpp
cn=aWsService,cn=Winsock Services,cn=system,dc=fabrikam,dc=com
```



```cpp
cn=aService,dc=itg,dc=fabrikam,dc=com
```



```cpp
www.fabrikam.com, ftp.fabrikam.com, ldap.fabrikam.com
```



```cpp
products.fabrikam.com
```

## -see-also

<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetspna">DsGetSPN</a>



<a href="/windows/desktop/AD/enumerations-in-active-directory-domain-services">Enumerations in Active Directory Domain Services</a>
