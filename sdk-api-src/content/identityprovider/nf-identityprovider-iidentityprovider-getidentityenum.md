---
UID: NF:identityprovider.IIdentityProvider.GetIdentityEnum
title: IIdentityProvider::GetIdentityEnum (identityprovider.h)
description: Retrieves an IEnumUnknown interface pointer that can be used to enumerate identities.
helpviewer_keywords: ["GetIdentityEnum","GetIdentityEnum method [Security]","GetIdentityEnum method [Security]","IIdentityProvider interface","IIdentityProvider interface [Security]","GetIdentityEnum method","IIdentityProvider.GetIdentityEnum","IIdentityProvider::GetIdentityEnum","identityprovider/IIdentityProvider::GetIdentityEnum","security.iidentityprovider_getidentityenum"]
old-location: security\iidentityprovider_getidentityenum.htm
tech.root: security
ms.assetid: 9e216959-7038-43cf-a57d-bee85d521f58
ms.date: 12/05/2018
ms.keywords: GetIdentityEnum, GetIdentityEnum method [Security], GetIdentityEnum method [Security],IIdentityProvider interface, IIdentityProvider interface [Security],GetIdentityEnum method, IIdentityProvider.GetIdentityEnum, IIdentityProvider::GetIdentityEnum, identityprovider/IIdentityProvider::GetIdentityEnum, security.iidentityprovider_getidentityenum
req.header: identityprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Identityprovider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IIdentityProvider::GetIdentityEnum
 - identityprovider/IIdentityProvider::GetIdentityEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Identityprovider.h
api_name:
 - IIdentityProvider.GetIdentityEnum
---

# IIdentityProvider::GetIdentityEnum


## -description

The <b>GetIdentityEnum</b> method retrieves an <a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a> interface pointer that can be used to enumerate identities.

## -parameters

### -param eIdentityType [in]

A value of the <a href="/windows/win32/api/identitycommon/ne-identitycommon-identity_type">IDENTITY_TYPE</a> enumeration that indicates the type of identities to enumerate.

### -param pFilterkey [in, optional]

A pointer to a property key that specifies a property. If the value of this parameter is not <b>NULL</b>, only identities that support the property specified by this parameter are enumerated.

### -param pFilterPropVarValue [in, optional]

A pointer to a property value. If the values of this parameter and the <i>pFilterkey</i> parameter are not <b>NULL</b>, only identities that have the property value specified by this parameter are enumerated.

### -param ppIdentityEnum [out]

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a> interface pointer that can be used to enumerate identities.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/identityprovider/nn-identityprovider-iidentityprovider">IIdentityProvider</a>