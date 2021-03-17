---
UID: NF:dsclient.IDsDisplaySpecifier.GetClassCreationInfo
title: IDsDisplaySpecifier::GetClassCreationInfo (dsclient.h)
description: Retrieves data about the class creation wizard objects for a given object class.
helpviewer_keywords: ["GetClassCreationInfo","GetClassCreationInfo method [Active Directory]","GetClassCreationInfo method [Active Directory]","IDsDisplaySpecifier interface","IDsDisplaySpecifier interface [Active Directory]","GetClassCreationInfo method","IDsDisplaySpecifier.GetClassCreationInfo","IDsDisplaySpecifier::GetClassCreationInfo","_glines_idsdisplayspecifier_getclasscreationinfo","ad.idsdisplayspecifier__getclasscreationinfo","ad.idsdisplayspecifier_getclasscreationinfo","dsclient/IDsDisplaySpecifier::GetClassCreationInfo"]
old-location: ad\idsdisplayspecifier_getclasscreationinfo.htm
tech.root: ad
ms.assetid: 23b88707-c4c3-47dd-a5bc-e325142602f5
ms.date: 12/05/2018
ms.keywords: GetClassCreationInfo, GetClassCreationInfo method [Active Directory], GetClassCreationInfo method [Active Directory],IDsDisplaySpecifier interface, IDsDisplaySpecifier interface [Active Directory],GetClassCreationInfo method, IDsDisplaySpecifier.GetClassCreationInfo, IDsDisplaySpecifier::GetClassCreationInfo, _glines_idsdisplayspecifier_getclasscreationinfo, ad.idsdisplayspecifier__getclasscreationinfo, ad.idsdisplayspecifier_getclasscreationinfo, dsclient/IDsDisplaySpecifier::GetClassCreationInfo
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
 - IDsDisplaySpecifier::GetClassCreationInfo
 - dsclient/IDsDisplaySpecifier::GetClassCreationInfo
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
 - IDsDisplaySpecifier.GetClassCreationInfo
---

# IDsDisplaySpecifier::GetClassCreationInfo


## -description

The <b>IDsDisplaySpecifier::GetClassCreationInfo</b> method retrieves data about the class creation wizard objects for a given object class.

## -parameters

### -param pszObjectClass [in]

Pointer to a null-terminated Unicode string that contains the name of the attribute to obtain the <b>ADsType</b>  for.

### -param ppdscci [in]

Pointer to a <a href="/windows/desktop/api/dsclient/ns-dsclient-dsclasscreationinfo">DSCLASSCREATIONINFO</a> structure pointer that receives  the class creation data. This memory is allocated by this method. The caller must free this memory using <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> when it is no longer required.

## -returns

Returns a standard <b>HRESULT</b> value including the following.

## -see-also

<a href="/windows/desktop/api/dsclient/ns-dsclient-dsclasscreationinfo">DSCLASSCREATIONINFO</a>



<a href="/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/dsclient/nn-dsclient-idsdisplayspecifier">IDsDisplaySpecifier</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>