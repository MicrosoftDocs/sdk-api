---
UID: NF:wininet.InternetClearAllPerSiteCookieDecisions
title: InternetClearAllPerSiteCookieDecisions function
author: windows-sdk-content
description: Clears all decisions that were made about cookies on a site by site basis.
old-location: wininet\internetclearallpersitecookiedecisions.htm
old-project: WinInet
ms.assetid: 980df63e-70b8-44d3-b98a-b7c8a3e395c6
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: InternetClearAllPerSiteCookieDecisions, InternetClearAllPerSiteCookieDecisions function [WinINet], wininet.internetclearallpersitecookiedecisions, wininet/InternetClearAllPerSiteCookieDecisions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - InternetClearAllPerSiteCookieDecisions
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# InternetClearAllPerSiteCookieDecisions function


## -description


Clears all decisions that were made about cookies on a site by site basis.


## -parameters






## -returns



Returns <b>TRUE</b> if all decisions were cleared and <b>FALSE</b> otherwise.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/de1db7e6-21f4-4bbb-b4fc-277bbd01f32c">InternetEnumPerSiteCookieDecision</a>



<a href="https://msdn.microsoft.com/04fa4c33-077c-4b16-8170-c3770783c98a">InternetGetPerSiteCookieDecisions</a>



<a href="https://msdn.microsoft.com/c25699b9-f79a-443b-b9a4-461c379fa8e4">InternetSetPerSiteCookieDecisions</a>



<a href="https://msdn.microsoft.com/530a86a0-bb67-406a-be83-5f2b463a1aa1">PrivacyGetZonePreferenceW</a>



<a href="https://msdn.microsoft.com/29c8dbc0-052e-40f4-a036-cb647d920055">PrivacySetZonePreferenceW</a>
 

 

