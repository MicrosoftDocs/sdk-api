---
UID: NF:dsclient.IDsDisplaySpecifier.EnumClassAttributes
title: IDsDisplaySpecifier::EnumClassAttributes (dsclient.h)
description: Enumerates the attributes for a given object class.
helpviewer_keywords: ["EnumClassAttributes","EnumClassAttributes method [Active Directory]","EnumClassAttributes method [Active Directory]","IDsDisplaySpecifier interface","IDsDisplaySpecifier interface [Active Directory]","EnumClassAttributes method","IDsDisplaySpecifier.EnumClassAttributes","IDsDisplaySpecifier::EnumClassAttributes","_glines_idsdisplayspecifier_enumclassattributes","ad.idsdisplayspecifier__enumclassattributes","ad.idsdisplayspecifier_enumclassattributes","dsclient/IDsDisplaySpecifier::EnumClassAttributes"]
old-location: ad\idsdisplayspecifier_enumclassattributes.htm
tech.root: ad
ms.assetid: 78b8e280-454c-4db7-9037-ea7e42798323
ms.date: 12/05/2018
ms.keywords: EnumClassAttributes, EnumClassAttributes method [Active Directory], EnumClassAttributes method [Active Directory],IDsDisplaySpecifier interface, IDsDisplaySpecifier interface [Active Directory],EnumClassAttributes method, IDsDisplaySpecifier.EnumClassAttributes, IDsDisplaySpecifier::EnumClassAttributes, _glines_idsdisplayspecifier_enumclassattributes, ad.idsdisplayspecifier__enumclassattributes, ad.idsdisplayspecifier_enumclassattributes, dsclient/IDsDisplaySpecifier::EnumClassAttributes
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDsDisplaySpecifier::EnumClassAttributes
 - dsclient/IDsDisplaySpecifier::EnumClassAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsadmin.dll
api_name:
 - IDsDisplaySpecifier.EnumClassAttributes
---

# IDsDisplaySpecifier::EnumClassAttributes


## -description

The <b>IDsDisplaySpecifier::EnumClassAttributes</b> method enumerates the attributes for a given object class. The enumeration provides both the LDAP and localized names of each attribute.

## -parameters

### -param pszObjectClass [in]

Pointer to a null-terminated Unicode string that contains the name of the object class to enumerate the attributes for. Examples of the object class name are "user" and "container".

### -param pcbEnum [in]

Pointer to an application-supplied <a href="/windows/desktop/api/dsclient/nc-dsclient-lpdsenumattributes">DSEnumAttributesCallback</a> function that is called once for each enumerated attribute.

### -param lParam [in]

Contains an application-defined  parameter passed as the <i>lParam</i> parameter in the <a href="/windows/desktop/api/dsclient/nc-dsclient-lpdsenumattributes">DSEnumAttributesCallback</a> function.

## -returns

Returns a standard <b>HRESULT</b> value including the following.

## -see-also

<a href="/windows/desktop/api/dsclient/nc-dsclient-lpdsenumattributes">DSEnumAttributesCallback</a>



<a href="/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/dsclient/nn-dsclient-idsdisplayspecifier">IDsDisplaySpecifier</a>