---
UID: NF:wininet.InternetGetPerSiteCookieDecisionW
title: InternetGetPerSiteCookieDecisionW function
author: windows-sdk-content
description: Retrieves a decision on cookies for a given domain.
old-location: wininet\internetgetpersitecookiedecision.htm
tech.root: wininet
ms.assetid: 04fa4c33-077c-4b16-8170-c3770783c98a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: InternetGetPerSiteCookieDecision, InternetGetPerSiteCookieDecision function [WinINet], InternetGetPerSiteCookieDecisionA, InternetGetPerSiteCookieDecisionW, wininet.internetgetpersitecookiedecision, wininet/InternetGetPerSiteCookieDecision, wininet/InternetGetPerSiteCookieDecisionA, wininet/InternetGetPerSiteCookieDecisionW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InternetGetPerSiteCookieDecisionW function


## -description


Retrieves a decision on cookies for a given domain.


## -parameters




### -param pchHostName [in]

An <b>LPCTSTR</b> that points to a string containing a domain.


### -param pResult [out]

A pointer to an <b>unsigned long</b> that contains one of the <a href="https://msdn.microsoft.com/3f43f492-3133-4cbd-9ab9-3c9600ef5263">InternetCookieState</a> enumeration values.



## -returns



Returns <b>TRUE</b> if the decision was retrieved and <b>FALSE</b> otherwise.





## -remarks



A return value of <b>FALSE</b> may indicate that the domain <i>pchHostName</i> does not have any site-specific cookie regulations.



WinINet minimizes the domain specified in the <i>pchHostName</i> parameter and sets the cookie policy on the minimimum legal domain. For example, if the specified host name is  widgets.microsoft.com, the policy is set on the minimized host name microsoft.com.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/980df63e-70b8-44d3-b98a-b7c8a3e395c6">InternetClearAllPerSiteCookieDecisions</a>



<a href="https://msdn.microsoft.com/de1db7e6-21f4-4bbb-b4fc-277bbd01f32c">InternetEnumPerSiteCookieDecision</a>



<a href="https://msdn.microsoft.com/c25699b9-f79a-443b-b9a4-461c379fa8e4">InternetSetPerSiteCookieDecision</a>



<a href="https://msdn.microsoft.com/530a86a0-bb67-406a-be83-5f2b463a1aa1">PrivacyGetZonePreferenceW</a>



<a href="https://msdn.microsoft.com/29c8dbc0-052e-40f4-a036-cb647d920055">PrivacySetZonePreferenceW</a>
 

 

