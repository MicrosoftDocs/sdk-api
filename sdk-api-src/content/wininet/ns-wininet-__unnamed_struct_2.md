---
UID: NS:wininet.__unnamed_struct_2
title: InternetCookieHistory
author: windows-driver-content
description: The InternetCookieHistory structure contains the cookie history.
old-location: wininet\internetcookiehistory.htm
old-project: WinInet
ms.assetid: c3aba5be-da66-4471-98e7-95fa5bd88c99
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: InternetCookieHistory, InternetCookieHistory structure [WinINet], wininet.internetcookiehistory, wininet/InternetCookieHistory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: InternetCookieHistory
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wininet.h
api_name:
-	InternetCookieHistory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# InternetCookieHistory structure


## -description


The <b>InternetCookieHistory</b> structure contains the cookie history.


## -struct-fields




### -field fAccepted

If true, the cookie was accepted.


### -field fLeashed

If true, the cookie was leashed.


### -field fDowngraded

If true, the cookie was downgraded.


### -field fRejected

If true, the cookie was rejected.


## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>


