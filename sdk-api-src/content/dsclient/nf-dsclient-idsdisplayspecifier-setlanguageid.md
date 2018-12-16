---
UID: NF:dsclient.IDsDisplaySpecifier.SetLanguageID
title: IDsDisplaySpecifier::SetLanguageID
author: windows-sdk-content
description: Changes the locale used by the IDsDisplaySpecifier object to a specified language.
old-location: ad\idsdisplayspecifier_setlanguageid.htm
tech.root: ad
ms.assetid: 306538a4-dccc-4f4f-89fa-491d08718d14
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDsDisplaySpecifier interface [Active Directory],SetLanguageID method, IDsDisplaySpecifier.SetLanguageID, IDsDisplaySpecifier::SetLanguageID, SetLanguageID, SetLanguageID method [Active Directory], SetLanguageID method [Active Directory],IDsDisplaySpecifier interface, _glines_idsdisplayspecifier_setlanguageid, ad.idsdisplayspecifier__setlanguageid, ad.idsdisplayspecifier_setlanguageid, dsclient/IDsDisplaySpecifier::SetLanguageID
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
 - IDsDisplaySpecifier.SetLanguageID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsDisplaySpecifier::SetLanguageID


## -description


The <b>IDsDisplaySpecifier::SetLanguageID</b> method  changes the locale used by the  <a href="https://msdn.microsoft.com/a6ac7006-73b8-4673-89d6-8285453481d3">IDsDisplaySpecifier</a> object to a specified language.


## -parameters




### -param langid [in]

Contains the language identifier used by the <a href="https://msdn.microsoft.com/a6ac7006-73b8-4673-89d6-8285453481d3">IDsDisplaySpecifier</a> object. If this parameter is zero, this method calls the 
<a href="https://msdn.microsoft.com/0de3a2d8-e595-4068-805c-b9bcba7ada91">GetUserDefaultUILanguage</a> function to retrieve the current user language identifier and uses that locale.


## -returns



This method always returns <b>S_OK</b>.




## -remarks



During object creation, the <a href="https://msdn.microsoft.com/a6ac7006-73b8-4673-89d6-8285453481d3">IDsDisplaySpecifier</a> object obtains the locale by calling <a href="https://msdn.microsoft.com/0de3a2d8-e595-4068-805c-b9bcba7ada91">GetUserDefaultUILanguage</a>. This method enables the object user to change the locale used with the display specifiers.




## -see-also




<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/0de3a2d8-e595-4068-805c-b9bcba7ada91">GetUserDefaultUILanguage</a>



<a href="https://msdn.microsoft.com/a6ac7006-73b8-4673-89d6-8285453481d3">IDsDisplaySpecifier</a>
 

 

