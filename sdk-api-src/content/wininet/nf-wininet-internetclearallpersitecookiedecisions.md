---
UID: NF:wininet.InternetClearAllPerSiteCookieDecisions
title: InternetClearAllPerSiteCookieDecisions function (wininet.h)
author: windows-sdk-content
description: Clears all decisions that were made about cookies on a site by site basis.
old-location: wininet\internetclearallpersitecookiedecisions.htm
tech.root: wininet
ms.assetid: 980df63e-70b8-44d3-b98a-b7c8a3e395c6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InternetClearAllPerSiteCookieDecisions, InternetClearAllPerSiteCookieDecisions function [WinINet], wininet.internetclearallpersitecookiedecisions, wininet/InternetClearAllPerSiteCookieDecisions
ms.topic: function
f1_keywords: 
 - "wininet/InternetClearAllPerSiteCookieDecisions"
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - InternetClearAllPerSiteCookieDecisions
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InternetClearAllPerSiteCookieDecisions function


## -description


Clears all decisions that were made about cookies on a site by site basis.


## -parameters






## -returns



Returns <b>TRUE</b> if all decisions were cleared and <b>FALSE</b> otherwise.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetenumpersitecookiedecisiona">InternetEnumPerSiteCookieDecision</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetgetpersitecookiedecisiona">InternetGetPerSiteCookieDecisions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetsetpersitecookiedecisiona">InternetSetPerSiteCookieDecisions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-privacygetzonepreferencew">PrivacyGetZonePreferenceW</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-privacysetzonepreferencew">PrivacySetZonePreferenceW</a>
 

 

