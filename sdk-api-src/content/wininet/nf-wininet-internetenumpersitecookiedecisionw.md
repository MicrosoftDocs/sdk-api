---
UID: NF:wininet.InternetEnumPerSiteCookieDecisionW
title: InternetEnumPerSiteCookieDecisionW function
author: windows-sdk-content
description: Retrieves the domains and cookie settings of websites for which site-specific cookie regulations are set.
old-location: wininet\internetenumpersitecookiedecision.htm
old-project: wininet
ms.assetid: de1db7e6-21f4-4bbb-b4fc-277bbd01f32c
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: InternetEnumPerSiteCookieDecision, InternetEnumPerSiteCookieDecision function [WinINet], InternetEnumPerSiteCookieDecisionA, InternetEnumPerSiteCookieDecisionW, wininet.internetenumpersitecookiedecision, winineti/InternetEnumPerSiteCookieDecision, winineti/InternetEnumPerSiteCookieDecisionA, winineti/InternetEnumPerSiteCookieDecisionW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wininet.h
req.include-header: Wininet.h, Winineti.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetEnumPerSiteCookieDecisionW (Unicode) and InternetEnumPerSiteCookieDecisionA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InternetCookieState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetEnumPerSiteCookieDecision
 - InternetEnumPerSiteCookieDecisionA
 - InternetEnumPerSiteCookieDecisionW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# InternetEnumPerSiteCookieDecisionW function


## -description


Retrieves the domains and cookie settings of websites for which site-specific cookie regulations are set.


## -parameters




### -param pszSiteName [out]

An <b>LPSTR</b> that receives a string specifying a website domain.


### -param pcSiteNameSize [in, out]

A pointer to an unsigned long that specifies the size of the <i>pcSiteNameSize</i> parameter provided to the InternetEnumPerSiteCookieDecision function when it is called. When <b>InternetEnumPerSiteCookieDecision</b> returns, <i>pcSiteNameSize</i> receives the actual length of the domain string returned in <i>pszSiteName</i>. 


### -param pdwDecision [out]

Pointer to an unsigned long that receives the <a href="https://msdn.microsoft.com/3f43f492-3133-4cbd-9ab9-3c9600ef5263">InternetCookieState</a> enumeration value corresponding to <i>pszSiteName</i>.


### -param dwIndex [in]

An unsigned long that specifies the index of the website and corresponding cookie setting to retrieve.



## -returns



<b>TRUE</b> if the function retrieved the cookie setting for the given domain; otherwise, false. <b>FALSE</b>.





## -remarks



<b>InternetEnumPerSiteCookieDecision</b> should be initially called with <i>dwIndex</i> equal to 0. Incrementing the <i>dwIndex</i> parameter steps through the list of websites and cookie settings. The end of the list is reached when <b>InternetEnumPerSiteCookieDecision</b> returns <b>FALSE</b> and produces the wininet error, <b>ERROR_NO_MORE_ITEMS</b>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/980df63e-70b8-44d3-b98a-b7c8a3e395c6">InternetClearAllPerSiteCookieDecisions</a>



<a href="https://msdn.microsoft.com/04fa4c33-077c-4b16-8170-c3770783c98a">InternetGetPerSiteCookieDecision</a>



<a href="https://msdn.microsoft.com/c25699b9-f79a-443b-b9a4-461c379fa8e4">InternetSetPerSiteCookieDecision</a>



<a href="https://msdn.microsoft.com/530a86a0-bb67-406a-be83-5f2b463a1aa1">PrivacyGetZonePreferenceW</a>



<a href="https://msdn.microsoft.com/29c8dbc0-052e-40f4-a036-cb647d920055">PrivacySetZonePreferenceW</a>
 

 

