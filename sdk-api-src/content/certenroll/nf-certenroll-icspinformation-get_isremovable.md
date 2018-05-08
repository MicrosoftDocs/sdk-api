---
UID: NF:certenroll.ICspInformation.get_IsRemovable
title: ICspInformation::get_IsRemovable
author: windows-driver-content
description: Retrieves a Boolean value that specifies whether the token that contains the key can be removed.
old-location: security\icspinformation_isremovable_property.htm
old-project: SecCertEnroll
ms.assetid: ee67670b-80a9-4637-a5ed-84d3430853ea
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ICspInformation interface [Security],IsRemovable property, ICspInformation.IsRemovable, ICspInformation.get_IsRemovable, ICspInformation::IsRemovable, ICspInformation::get_IsRemovable, IsRemovable property [Security], IsRemovable property [Security],ICspInformation interface, certenroll/ICspInformation::IsRemovable, certenroll/ICspInformation::get_IsRemovable, get_IsRemovable, security.icspinformation_isremovable_property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	ICspInformation.IsRemovable
-	ICspInformation.get_IsRemovable
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspInformation::get_IsRemovable


## -description


The <b>IsRemovable</b> property retrieves a Boolean value that specifies whether the token that contains the key can be removed.

This property is read-only.


## -parameters


## -remarks



Operator cards and  smart cards are examples of removable tokens that can contain keys. For example, the following providers return true for this property value:<ul>
<li>Microsoft Smart Card Key Storage Provider</li>
<li>Microsoft Base Smart Card Crypto Provider</li>
</ul>


The Certificate Enrollment service assumes that a provider is a smart card provider if both the <a href="https://msdn.microsoft.com/d69ade8c-3b74-4391-9048-6511f3d7e9fa">IsHardwareDevice</a> and <a href="https://msdn.microsoft.com/50f78dcc-4d32-40c9-8153-f0b6ac72c03b">IsSoftwareDevice</a> properties are set, or if the <b>IsRemovable</b> property is set.




## -see-also




<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>
 

 

