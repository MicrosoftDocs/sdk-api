---
UID: NF:wininet.InternetSetPerSiteCookieDecisionA
title: InternetSetPerSiteCookieDecisionA function (wininet.h)
description: Sets a decision on cookies for a given domain.helpviewer_keywords: ["InternetSetPerSiteCookieDecision","InternetSetPerSiteCookieDecision function [WinINet]","InternetSetPerSiteCookieDecisionA","InternetSetPerSiteCookieDecisionW","wininet.internetsetpersitecookiedecision","wininet/InternetSetPerSiteCookieDecision","wininet/InternetSetPerSiteCookieDecisionA","wininet/InternetSetPerSiteCookieDecisionW"]
old-location: wininet\internetsetpersitecookiedecision.htm
tech.root: wininet
ms.assetid: c25699b9-f79a-443b-b9a4-461c379fa8e4
ms.date: 12/05/2018
ms.keywords: InternetSetPerSiteCookieDecision, InternetSetPerSiteCookieDecision function [WinINet], InternetSetPerSiteCookieDecisionA, InternetSetPerSiteCookieDecisionW, wininet.internetsetpersitecookiedecision, wininet/InternetSetPerSiteCookieDecision, wininet/InternetSetPerSiteCookieDecisionA, wininet/InternetSetPerSiteCookieDecisionW
f1_keywords:
- wininet/InternetSetPerSiteCookieDecision
dev_langs:
- c++
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetSetPerSiteCookieDecisionW (Unicode) and InternetSetPerSiteCookieDecisionA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wininet.dll
api_name:
- InternetSetPerSiteCookieDecision
- InternetSetPerSiteCookieDecisionA
- InternetSetPerSiteCookieDecisionW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InternetSetPerSiteCookieDecisionA function


## -description


Sets a decision on cookies for a given domain.


## -parameters




### -param pchHostName [in]

An <b>LPCTSTR</b> that points to a string containing a domain.


### -param dwDecision [in]

A value of type <b>DWORD</b> that contains one of the <a href="https://docs.microsoft.com/windows/win32/api/wininet/ne-wininet-internet_scheme">InternetCookieState</a> enumeration values.


## -returns



Returns <b>TRUE</b> if the decision is set and <b>FALSE</b> otherwise.





## -remarks



WinINet minimizes the domain specified in the <i>pchHostName</i> parameter and sets the cookie policy on the minimimum legal domain. For example, if the specified host name is  widgets.microsoft.com, the policy is set on the minimized host name microsoft.com.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetclearallpersitecookiedecisions">InternetClearAllPerSiteCookieDecisions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetenumpersitecookiedecisiona">InternetEnumPerSiteCookieDecision</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetgetpersitecookiedecisiona">InternetGetPerSiteCookieDecision</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-privacygetzonepreferencew">PrivacyGetZonePreferenceW</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-privacysetzonepreferencew">PrivacySetZonePreferenceW</a>
 

 

