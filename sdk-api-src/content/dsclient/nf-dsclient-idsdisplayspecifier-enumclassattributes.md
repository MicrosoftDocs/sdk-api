---
UID: NF:dsclient.IDsDisplaySpecifier.EnumClassAttributes
title: IDsDisplaySpecifier::EnumClassAttributes (dsclient.h)
author: windows-sdk-content
description: Enumerates the attributes for a given object class.
old-location: ad\idsdisplayspecifier_enumclassattributes.htm
tech.root: ad
ms.assetid: 78b8e280-454c-4db7-9037-ea7e42798323
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumClassAttributes, EnumClassAttributes method [Active Directory], EnumClassAttributes method [Active Directory],IDsDisplaySpecifier interface, IDsDisplaySpecifier interface [Active Directory],EnumClassAttributes method, IDsDisplaySpecifier.EnumClassAttributes, IDsDisplaySpecifier::EnumClassAttributes, _glines_idsdisplayspecifier_enumclassattributes, ad.idsdisplayspecifier__enumclassattributes, ad.idsdisplayspecifier_enumclassattributes, dsclient/IDsDisplaySpecifier::EnumClassAttributes
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
 - IDsDisplaySpecifier.EnumClassAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDsDisplaySpecifier::EnumClassAttributes


## -description


The <b>IDsDisplaySpecifier::EnumClassAttributes</b> method enumerates the attributes for a given object class. The enumeration provides both the LDAP and localized names of each attribute.


## -parameters




### -param pszObjectClass [in]

Pointer to a null-terminated Unicode string that contains the name of the object class to enumerate the attributes for. Examples of the object class name are "user" and "container".


### -param pcbEnum [in]

Pointer to an application-supplied <a href="https://msdn.microsoft.com/f4f35119-9ffc-4fe9-aea1-2d4a5d4edd0b">DSEnumAttributesCallback</a> function that is called once for each enumerated attribute.


### -param lParam [in]

Contains an application-defined  parameter passed as the <i>lParam</i> parameter in the <a href="https://msdn.microsoft.com/f4f35119-9ffc-4fe9-aea1-2d4a5d4edd0b">DSEnumAttributesCallback</a> function.


## -returns



Returns a standard <b>HRESULT</b> value including the following.




## -see-also




<a href="https://msdn.microsoft.com/f4f35119-9ffc-4fe9-aea1-2d4a5d4edd0b">DSEnumAttributesCallback</a>



<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/a6ac7006-73b8-4673-89d6-8285453481d3">IDsDisplaySpecifier</a>
 

 

