---
UID: NF:dsclient.IDsDisplaySpecifier.GetFriendlyAttributeName
title: IDsDisplaySpecifier::GetFriendlyAttributeName
author: windows-sdk-content
description: The IDsDisplaySpecifier::GetFriendlyAttributeName method retrieves from the localized name of an attribute of a given object class.
old-location: ad\idsdisplayspecifier_getfriendlyattributename.htm
tech.root: ad
ms.assetid: 6a4551ec-0b73-4119-8fdd-1e1952f60bd2
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: GetFriendlyAttributeName, GetFriendlyAttributeName method [Active Directory], GetFriendlyAttributeName method [Active Directory],IDsDisplaySpecifier interface, IDsDisplaySpecifier interface [Active Directory],GetFriendlyAttributeName method, IDsDisplaySpecifier.GetFriendlyAttributeName, IDsDisplaySpecifier::GetFriendlyAttributeName, _glines_idsdisplayspecifier_getfriendlyattributename, ad.idsdisplayspecifier__getfriendlyattributename, ad.idsdisplayspecifier_getfriendlyattributename, dsclient/IDsDisplaySpecifier::GetFriendlyAttributeName
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
 - IDsDisplaySpecifier.GetFriendlyAttributeName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsDisplaySpecifier::GetFriendlyAttributeName


## -description


The <b>IDsDisplaySpecifier::GetFriendlyAttributeName</b> method retrieves from the localized name of an attribute of a given object class.


## -parameters




### -param pszObjectClass [in]

Pointer to a null-terminated Unicode string that contains the name of the object class to obtain the localized attribute name for. Examples of the object class name are "user" and "container".


### -param pszAttributeName [in]

Pointer to a null-terminated Unicode string that contains the name of the attribute to obtain the localized name for.


### -param pszBuffer [in]

Pointer to a wide character buffer that receives the name string. This buffer must be at least <i>cchBuffer</i> wide characters in length.


### -param cchBuffer [in]

Contains the size of the <i>pszBuffer</i> buffer, in wide characters, including the terminating <b>NULL</b> character. If the name exceeds this number of characters, the name is truncated.


## -returns



Returns a standard  <b>HRESULT</b> value, including the following.




## -remarks



This method looks up the display specifier of the class to check the <b>attributeNames</b> property for an attribute name pair that matches the given attribute name. If no match is  found, the input attribute name is returned.




## -see-also




<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/a6ac7006-73b8-4673-89d6-8285453481d3">IDsDisplaySpecifier</a>
 

 

