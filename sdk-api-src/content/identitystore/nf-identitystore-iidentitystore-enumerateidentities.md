---
UID: NF:identitystore.IIdentityStore.EnumerateIdentities
title: IIdentityStore::EnumerateIdentities
author: windows-sdk-content
description: Gets a pointer to an IEnumUnknown interface pointer that can be used to enumerate identities across identity providers.
old-location: security\iidentitystore_enumerateidentities.htm
tech.root: secauthn
ms.assetid: df1a53e0-6296-49ed-b0f0-85e9dc9ab947
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: EnumerateIdentities, EnumerateIdentities method [Security], EnumerateIdentities method [Security],IIdentityStore interface, IIdentityStore interface [Security],EnumerateIdentities method, IIdentityStore.EnumerateIdentities, IIdentityStore::EnumerateIdentities, identitystore/IIdentityStore::EnumerateIdentities, security.iidentitystore_enumerateidentities
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIdentityStore::EnumerateIdentities


## -description


The <b>EnumerateIdentities</b> method gets a pointer to an <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms683764">IEnumUnknown</a> interface pointer that can be used to enumerate identities across identity providers.


## -parameters




### -param eIdentityType [in]

A value of the <a href="https://msdn.microsoft.com/en-us/library/Dd401667(v=VS.85).aspx">IDENTITY_TYPE</a> enumeration that indicates the type of identities to enumerate.


### -param pFilterkey [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure that specifies a property. If the value of this parameter is not <b>NULL</b>, only identities that support the property specified by this parameter are enumerated.


### -param pFilterPropVarValue [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. If the values of this parameter and the <i>pFilterkey</i> parameters are not <b>NULL</b>, only identities that have the property value specified by this parameter are enumerated.


### -param ppIdentityEnum [out]

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms683764">IEnumUnknown</a> interface pointer that can be used to enumerate identities.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/f7f0f103-411b-4fbd-9ed5-30c6ab2f0ab6">IIdentityStore</a>
 

 

