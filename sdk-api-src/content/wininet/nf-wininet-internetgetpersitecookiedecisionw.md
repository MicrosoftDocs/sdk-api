---
UID: NF:wininet.InternetGetPerSiteCookieDecisionW
title: InternetGetPerSiteCookieDecisionW function (wininet.h)
description: Retrieves a decision on cookies for a given domain. (Unicode)
helpviewer_keywords: ["InternetGetPerSiteCookieDecision", "InternetGetPerSiteCookieDecision function [WinINet]", "InternetGetPerSiteCookieDecisionW", "wininet.internetgetpersitecookiedecision", "wininet/InternetGetPerSiteCookieDecision", "wininet/InternetGetPerSiteCookieDecisionW"]
old-location: wininet\internetgetpersitecookiedecision.htm
tech.root: wininet
ms.assetid: 04fa4c33-077c-4b16-8170-c3770783c98a
ms.date: 12/05/2018
ms.keywords: InternetGetPerSiteCookieDecision, InternetGetPerSiteCookieDecision function [WinINet], InternetGetPerSiteCookieDecisionA, InternetGetPerSiteCookieDecisionW, wininet.internetgetpersitecookiedecision, wininet/InternetGetPerSiteCookieDecision, wininet/InternetGetPerSiteCookieDecisionA, wininet/InternetGetPerSiteCookieDecisionW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetGetPerSiteCookieDecisionW (Unicode) and InternetGetPerSiteCookieDecisionA (ANSI)
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
 - InternetGetPerSiteCookieDecisionW
 - wininet/InternetGetPerSiteCookieDecisionW
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
 - InternetGetPerSiteCookieDecision
 - InternetGetPerSiteCookieDecisionA
 - InternetGetPerSiteCookieDecisionW
---

# InternetGetPerSiteCookieDecisionW function


## -description

Retrieves a decision on cookies for a given domain.

## -parameters

### -param pchHostName [in]

An <b>LPCTSTR</b> that points to a string containing a domain.

### -param pResult [out]

A pointer to an <b>unsigned long</b> that contains one of the <a href="/windows/win32/api/wininet/ne-wininet-internet_scheme">InternetCookieState</a> enumeration values.

## -returns

Returns <b>TRUE</b> if the decision was retrieved and <b>FALSE</b> otherwise.

## -remarks

A return value of <b>FALSE</b> may indicate that the domain <i>pchHostName</i> does not have any site-specific cookie regulations.



WinINet minimizes the domain specified in the <i>pchHostName</i> parameter and sets the cookie policy on the minimum legal domain. For example, if the specified host name is  widgets.microsoft.com, the policy is set on the minimized host name microsoft.com.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetGetPerSiteCookieDecision as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-internetclearallpersitecookiedecisions">InternetClearAllPerSiteCookieDecisions</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetenumpersitecookiedecisiona">InternetEnumPerSiteCookieDecision</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetsetpersitecookiedecisiona">InternetSetPerSiteCookieDecision</a>



<a href="/windows/desktop/api/wininet/nf-wininet-privacygetzonepreferencew">PrivacyGetZonePreferenceW</a>



<a href="/windows/desktop/api/wininet/nf-wininet-privacysetzonepreferencew">PrivacySetZonePreferenceW</a>
