---
UID: NF:dsclient.IDsDisplaySpecifier.GetFriendlyClassName
title: IDsDisplaySpecifier::GetFriendlyClassName (dsclient.h)
description: The IDsDisplaySpecifier::GetFriendlyClassName method retrieves the localized name for an object class.
helpviewer_keywords: ["GetFriendlyClassName","GetFriendlyClassName method [Active Directory]","GetFriendlyClassName method [Active Directory]","IDsDisplaySpecifier interface","IDsDisplaySpecifier interface [Active Directory]","GetFriendlyClassName method","IDsDisplaySpecifier.GetFriendlyClassName","IDsDisplaySpecifier::GetFriendlyClassName","_glines_idsdisplayspecifier_getfriendlyclassname","ad.idsdisplayspecifier__getfriendlyclassname","ad.idsdisplayspecifier_getfriendlyclassname","dsclient/IDsDisplaySpecifier::GetFriendlyClassName"]
old-location: ad\idsdisplayspecifier_getfriendlyclassname.htm
tech.root: ad
ms.assetid: 192e2a57-6bde-4357-893e-37f466588b55
ms.date: 12/05/2018
ms.keywords: GetFriendlyClassName, GetFriendlyClassName method [Active Directory], GetFriendlyClassName method [Active Directory],IDsDisplaySpecifier interface, IDsDisplaySpecifier interface [Active Directory],GetFriendlyClassName method, IDsDisplaySpecifier.GetFriendlyClassName, IDsDisplaySpecifier::GetFriendlyClassName, _glines_idsdisplayspecifier_getfriendlyclassname, ad.idsdisplayspecifier__getfriendlyclassname, ad.idsdisplayspecifier_getfriendlyclassname, dsclient/IDsDisplaySpecifier::GetFriendlyClassName
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
 - IDsDisplaySpecifier::GetFriendlyClassName
 - dsclient/IDsDisplaySpecifier::GetFriendlyClassName
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
 - IDsDisplaySpecifier.GetFriendlyClassName
---

# IDsDisplaySpecifier::GetFriendlyClassName


## -description

The <b>IDsDisplaySpecifier::GetFriendlyClassName</b> method retrieves the localized name for an object class.

## -parameters

### -param pszObjectClass [in]

Pointer to a null-terminated Unicode string that contains the name of the object class to obtain the name of. Examples of the object class name are "user" and "container".

### -param pszBuffer [in, out]

Pointer to a wide character buffer that receives the name string. This buffer must be at least <i>cchBuffer</i> wide characters in length.

### -param cchBuffer [in]

Contains the size of the <i>pszBuffer</i> buffer, in wide characters, including the terminating <b>NULL</b> character. If the name exceeds this number of characters, the name is truncated.

## -returns

Returns a standard  <b>HRESULT</b> value, including the following.

## -remarks

If no friendly name is set in the display specifiers for the object class, this method returns the name passed in <i>pszObjectClass</i>.

## -see-also

<a href="/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/dsclient/nn-dsclient-idsdisplayspecifier">IDsDisplaySpecifier</a>