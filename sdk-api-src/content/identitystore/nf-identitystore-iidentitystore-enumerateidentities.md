---
UID: NF:identitystore.IIdentityStore.EnumerateIdentities
title: IIdentityStore::EnumerateIdentities (identitystore.h)
author: windows-sdk-content
description: Gets a pointer to an IEnumUnknown interface pointer that can be used to enumerate identities across identity providers.
old-location: security\iidentitystore_enumerateidentities.htm
tech.root: SecAuthN
ms.assetid: df1a53e0-6296-49ed-b0f0-85e9dc9ab947
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumerateIdentities, EnumerateIdentities method [Security], EnumerateIdentities method [Security],IIdentityStore interface, IIdentityStore interface [Security],EnumerateIdentities method, IIdentityStore.EnumerateIdentities, IIdentityStore::EnumerateIdentities, identitystore/IIdentityStore::EnumerateIdentities, security.iidentitystore_enumerateidentities
ms.topic: method
f1_keywords:
- identitystore/IIdentityStore.EnumerateIdentities
req.header: identitystore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Identitystore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Identitystore.h
api_name:
- IIdentityStore.EnumerateIdentities
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIdentityStore::EnumerateIdentities


## -description


The <b>EnumerateIdentities</b> method gets a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a> interface pointer that can be used to enumerate identities across identity providers.


## -parameters




### -param eIdentityType [in]

A value of the <a href="https://docs.microsoft.com/windows/win32/api/identitycommon/ne-identitycommon-identity_type">IDENTITY_TYPE</a> enumeration that indicates the type of identities to enumerate.


### -param pFilterkey [in, optional]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure that specifies a property. If the value of this parameter is not <b>NULL</b>, only identities that support the property specified by this parameter are enumerated.


### -param pFilterPropVarValue [in, optional]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. If the values of this parameter and the <i>pFilterkey</i> parameters are not <b>NULL</b>, only identities that have the property value specified by this parameter are enumerated.


### -param ppIdentityEnum [out]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a> interface pointer that can be used to enumerate identities.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/identitystore/nn-identitystore-iidentitystore">IIdentityStore</a>
 

 

