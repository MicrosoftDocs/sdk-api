---
UID: NF:wininet.InternetEnumPerSiteCookieDecisionW
title: InternetEnumPerSiteCookieDecisionW function (wininet.h)
description: The InternetEnumPerSiteCookieDecisionW (Unicode) function (wininet.h) retrieves the domains and cookie settings of websites with set site-specific cookie regulations.
helpviewer_keywords: ["InternetEnumPerSiteCookieDecision", "InternetEnumPerSiteCookieDecision function [WinINet]", "InternetEnumPerSiteCookieDecisionW", "wininet.internetenumpersitecookiedecision"]
old-location: wininet\internetenumpersitecookiedecision.htm
tech.root: wininet
ms.assetid: de1db7e6-21f4-4bbb-b4fc-277bbd01f32c
ms.date: 08/10/2022
ms.keywords: InternetEnumPerSiteCookieDecision, InternetEnumPerSiteCookieDecision function [WinINet], InternetEnumPerSiteCookieDecisionA, InternetEnumPerSiteCookieDecisionW, wininet.internetenumpersitecookiedecision, winineti/InternetEnumPerSiteCookieDecision, winineti/InternetEnumPerSiteCookieDecisionA, winineti/InternetEnumPerSiteCookieDecisionW
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
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InternetEnumPerSiteCookieDecisionW
 - wininet/InternetEnumPerSiteCookieDecisionW
dev_langs:
 - c++
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

Pointer to an unsigned long that receives the <a href="/windows/win32/api/wininet/ne-wininet-internet_scheme">InternetCookieState</a> enumeration value corresponding to <i>pszSiteName</i>.

### -param dwIndex [in]

An unsigned long that specifies the index of the website and corresponding cookie setting to retrieve.

## -returns

<b>TRUE</b> if the function retrieved the cookie setting for the given domain; otherwise, false. <b>FALSE</b>.

## -remarks

<b>InternetEnumPerSiteCookieDecision</b> should be initially called with <i>dwIndex</i> equal to 0. Incrementing the <i>dwIndex</i> parameter steps through the list of websites and cookie settings. The end of the list is reached when <b>InternetEnumPerSiteCookieDecision</b> returns <b>FALSE</b> and produces the wininet error, <b>ERROR_NO_MORE_ITEMS</b>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetEnumPerSiteCookieDecision as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-internetclearallpersitecookiedecisions">InternetClearAllPerSiteCookieDecisions</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetgetpersitecookiedecisiona">InternetGetPerSiteCookieDecision</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetsetpersitecookiedecisiona">InternetSetPerSiteCookieDecision</a>



<a href="/windows/desktop/api/wininet/nf-wininet-privacygetzonepreferencew">PrivacyGetZonePreferenceW</a>



<a href="/windows/desktop/api/wininet/nf-wininet-privacysetzonepreferencew">PrivacySetZonePreferenceW</a>
