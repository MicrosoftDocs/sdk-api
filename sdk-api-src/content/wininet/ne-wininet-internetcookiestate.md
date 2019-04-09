---
UID: NE:wininet.__unnamed_enum_1
title: InternetCookieState (wininet.h)
author: windows-sdk-content
description: The InternetCookieState enumeration defines the state of the cookie.
old-location: wininet\internetcookiestate.htm
tech.root: wininet
ms.assetid: 3f43f492-3133-4cbd-9ab9-3c9600ef5263
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: COOKIE_STATE_ACCEPT, COOKIE_STATE_DOWNGRADE, COOKIE_STATE_LEASH, COOKIE_STATE_MAX, COOKIE_STATE_PROMPT, COOKIE_STATE_REJECT, COOKIE_STATE_UNKNOWN, InternetCookieState, InternetCookieState enumeration [WinINet], wininet.internetcookiestate, wininet/COOKIE_STATE_ACCEPT, wininet/COOKIE_STATE_DOWNGRADE, wininet/COOKIE_STATE_LEASH, wininet/COOKIE_STATE_MAX, wininet/COOKIE_STATE_PROMPT, wininet/COOKIE_STATE_REJECT, wininet/COOKIE_STATE_UNKNOWN, wininet/InternetCookieState
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - InternetCookieState
product: Windows
targetos: Windows
req.typenames: InternetCookieState
req.redist: 
---

# InternetCookieState enumeration


## -description


The <b>InternetCookieState</b> enumeration defines the state of the cookie.


## -enum-fields




### -field COOKIE_STATE_UNKNOWN

Reserved.


### -field COOKIE_STATE_ACCEPT

The cookies are accepted.


### -field COOKIE_STATE_PROMPT

The user is prompted to accept or deny the cookie.


### -field COOKIE_STATE_LEASH

Cookies are accepted only in the first-party context.


### -field COOKIE_STATE_DOWNGRADE

Cookies are accepted and become session cookies.


### -field COOKIE_STATE_REJECT

The cookies are rejected.


### -field COOKIE_STATE_MAX

Same as <b>COOKIE_STATE_REJECT</b>.


## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/de1db7e6-21f4-4bbb-b4fc-277bbd01f32c">InternetEnumPerSiteCookieDecision</a>



<a href="https://msdn.microsoft.com/04fa4c33-077c-4b16-8170-c3770783c98a">InternetGetPerSiteCookieDecision</a>



<a href="https://msdn.microsoft.com/c25699b9-f79a-443b-b9a4-461c379fa8e4">InternetSetPerSiteCookieDecision</a>
 

 

