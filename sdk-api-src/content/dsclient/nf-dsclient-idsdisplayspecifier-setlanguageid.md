---
UID: NF:dsclient.IDsDisplaySpecifier.SetLanguageID
title: IDsDisplaySpecifier::SetLanguageID (dsclient.h)
description: Changes the locale used by the IDsDisplaySpecifier object to a specified language.
helpviewer_keywords: ["IDsDisplaySpecifier interface [Active Directory]","SetLanguageID method","IDsDisplaySpecifier.SetLanguageID","IDsDisplaySpecifier::SetLanguageID","SetLanguageID","SetLanguageID method [Active Directory]","SetLanguageID method [Active Directory]","IDsDisplaySpecifier interface","_glines_idsdisplayspecifier_setlanguageid","ad.idsdisplayspecifier__setlanguageid","ad.idsdisplayspecifier_setlanguageid","dsclient/IDsDisplaySpecifier::SetLanguageID"]
old-location: ad\idsdisplayspecifier_setlanguageid.htm
tech.root: ad
ms.assetid: 306538a4-dccc-4f4f-89fa-491d08718d14
ms.date: 12/05/2018
ms.keywords: IDsDisplaySpecifier interface [Active Directory],SetLanguageID method, IDsDisplaySpecifier.SetLanguageID, IDsDisplaySpecifier::SetLanguageID, SetLanguageID, SetLanguageID method [Active Directory], SetLanguageID method [Active Directory],IDsDisplaySpecifier interface, _glines_idsdisplayspecifier_setlanguageid, ad.idsdisplayspecifier__setlanguageid, ad.idsdisplayspecifier_setlanguageid, dsclient/IDsDisplaySpecifier::SetLanguageID
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
 - IDsDisplaySpecifier::SetLanguageID
 - dsclient/IDsDisplaySpecifier::SetLanguageID
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
 - IDsDisplaySpecifier.SetLanguageID
---

# IDsDisplaySpecifier::SetLanguageID


## -description

The <b>IDsDisplaySpecifier::SetLanguageID</b> method  changes the locale used by the  <a href="/windows/desktop/api/dsclient/nn-dsclient-idsdisplayspecifier">IDsDisplaySpecifier</a> object to a specified language.

## -parameters

### -param langid [in]

Contains the language identifier used by the <a href="/windows/desktop/api/dsclient/nn-dsclient-idsdisplayspecifier">IDsDisplaySpecifier</a> object. If this parameter is zero, this method calls the 
<a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultuilanguage">GetUserDefaultUILanguage</a> function to retrieve the current user language identifier and uses that locale.

## -returns

This method always returns <b>S_OK</b>.

## -remarks

During object creation, the <a href="/windows/desktop/api/dsclient/nn-dsclient-idsdisplayspecifier">IDsDisplaySpecifier</a> object obtains the locale by calling <a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultuilanguage">GetUserDefaultUILanguage</a>. This method enables the object user to change the locale used with the display specifiers.

## -see-also

<a href="/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultuilanguage">GetUserDefaultUILanguage</a>



<a href="/windows/desktop/api/dsclient/nn-dsclient-idsdisplayspecifier">IDsDisplaySpecifier</a>