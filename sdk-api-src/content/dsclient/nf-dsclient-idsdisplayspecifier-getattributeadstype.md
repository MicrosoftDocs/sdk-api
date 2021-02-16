---
UID: NF:dsclient.IDsDisplaySpecifier.GetAttributeADsType
title: IDsDisplaySpecifier::GetAttributeADsType (dsclient.h)
description: Retrieves the attribute type for a given attribute.
helpviewer_keywords: ["GetAttributeADsType","GetAttributeADsType method [Active Directory]","GetAttributeADsType method [Active Directory]","IDsDisplaySpecifier interface","IDsDisplaySpecifier interface [Active Directory]","GetAttributeADsType method","IDsDisplaySpecifier.GetAttributeADsType","IDsDisplaySpecifier::GetAttributeADsType","_glines_idsdisplayspecifier_getattributeadstype","ad.idsdisplayspecifier__getattributeadstype","ad.idsdisplayspecifier_getattributeadstype","dsclient/IDsDisplaySpecifier::GetAttributeADsType"]
old-location: ad\idsdisplayspecifier_getattributeadstype.htm
tech.root: ad
ms.assetid: 4e9ecbee-b298-42a4-ad02-28bab9d99b6b
ms.date: 12/05/2018
ms.keywords: GetAttributeADsType, GetAttributeADsType method [Active Directory], GetAttributeADsType method [Active Directory],IDsDisplaySpecifier interface, IDsDisplaySpecifier interface [Active Directory],GetAttributeADsType method, IDsDisplaySpecifier.GetAttributeADsType, IDsDisplaySpecifier::GetAttributeADsType, _glines_idsdisplayspecifier_getattributeadstype, ad.idsdisplayspecifier__getattributeadstype, ad.idsdisplayspecifier_getattributeadstype, dsclient/IDsDisplaySpecifier::GetAttributeADsType
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
 - IDsDisplaySpecifier::GetAttributeADsType
 - dsclient/IDsDisplaySpecifier::GetAttributeADsType
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
 - IDsDisplaySpecifier.GetAttributeADsType
---

# IDsDisplaySpecifier::GetAttributeADsType


## -description

The <b>IDsDisplaySpecifier::GetAttributeADsType</b> method retrieves the attribute type for a given attribute.

## -parameters

### -param pszAttributeName [in]

Pointer to a null-terminated Unicode string that contains the name of the attribute to obtain the type  for.

## -returns

Returns one of the <a href="/windows/win32/api/iads/ne-iads-adstypeenum">ADSTYPEENUM</a> values that indicate the type of the attribute.

## -see-also

<a href="/windows/win32/api/iads/ne-iads-adstypeenum">ADSTYPEENUM</a>



<a href="/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/dsclient/nn-dsclient-idsdisplayspecifier">IDsDisplaySpecifier</a>