---
UID: NF:identityprovider.IIdentityProvider.GetIdentityEnum
title: IIdentityProvider::GetIdentityEnum
author: windows-driver-content
description: Retrieves an IEnumUnknown interface pointer that can be used to enumerate identities.
old-location: security\iidentityprovider_getidentityenum.htm
old-project: SecAuthN
ms.assetid: 9e216959-7038-43cf-a57d-bee85d521f58
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetIdentityEnum, GetIdentityEnum method [Security], GetIdentityEnum method [Security],IIdentityProvider interface, IIdentityProvider interface [Security],GetIdentityEnum method, IIdentityProvider.GetIdentityEnum, IIdentityProvider::GetIdentityEnum, identityprovider/IIdentityProvider::GetIdentityEnum, security.iidentityprovider_getidentityenum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: IDENTITY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Identityprovider.h
api_name:
-	IIdentityProvider.GetIdentityEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IIdentityProvider::GetIdentityEnum


## -description


The <b>GetIdentityEnum</b> method retrieves an <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms683764">IEnumUnknown</a> interface pointer that can be used to enumerate identities.


## -parameters




### -param eIdentityType [in]

A value of the <a href="https://msdn.microsoft.com/">IDENTITY_TYPE</a> enumeration that indicates the type of identities to enumerate.


### -param pFilterkey [in, optional]

A pointer to a property key that specifies a property. If the value of this parameter is not <b>NULL</b>, only identities that support the property specified by this parameter are enumerated.


### -param pFilterPropVarValue [in, optional]

A pointer to a property value. If the values of this parameter and the <i>pFilterkey</i> parameter are not <b>NULL</b>, only identities that have the property value specified by this parameter are enumerated.


### -param ppIdentityEnum [out]

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms683764">IEnumUnknown</a> interface pointer that can be used to enumerate identities.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/0f23e369-1501-4e72-94d1-dadb9dac5be6">IIdentityProvider</a>
 

 

