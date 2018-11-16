---
UID: NF:dsclient.IDsDisplaySpecifier.GetAttributeADsType
title: IDsDisplaySpecifier::GetAttributeADsType
author: windows-sdk-content
description: Retrieves the attribute type for a given attribute.
old-location: ad\idsdisplayspecifier_getattributeadstype.htm
tech.root: ad
ms.assetid: 4e9ecbee-b298-42a4-ad02-28bab9d99b6b
ms.author: windowssdkdev
ms.date: 11/14/2018
ms.keywords: GetAttributeADsType, GetAttributeADsType method [Active Directory], GetAttributeADsType method [Active Directory],IDsDisplaySpecifier interface, IDsDisplaySpecifier interface [Active Directory],GetAttributeADsType method, IDsDisplaySpecifier.GetAttributeADsType, IDsDisplaySpecifier::GetAttributeADsType, _glines_idsdisplayspecifier_getattributeadstype, ad.idsdisplayspecifier__getattributeadstype, ad.idsdisplayspecifier_getattributeadstype, dsclient/IDsDisplaySpecifier::GetAttributeADsType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dsclient.h
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
req.dll: Dsadmin.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsadmin.dll
api_name:
 - IDsDisplaySpecifier.GetAttributeADsType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dsclient.h
: 
- IDsDisplaySpecifier.GetAttributeADsType
: 
---

# IDsDisplaySpecifier::GetAttributeADsType


## -description


The <b>IDsDisplaySpecifier::GetAttributeADsType</b> method retrieves the attribute type for a given attribute.


## -parameters




### -param pszAttributeName [in]

Pointer to a null-terminated Unicode string that contains the name of the attribute to obtain the type  for.


## -returns



Returns one of the <a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a> values that indicate the type of the attribute.




## -see-also




<a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a>



<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/a6ac7006-73b8-4673-89d6-8285453481d3">IDsDisplaySpecifier</a>
 

 

