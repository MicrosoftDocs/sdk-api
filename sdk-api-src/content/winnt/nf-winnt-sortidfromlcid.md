---
UID: NF:winnt.SORTIDFROMLCID
title: SORTIDFROMLCID macro
author: windows-sdk-content
description: Retrieves a sort order identifier from a locale identifier.
old-location: intl\sortidfromlcid.htm
old-project: Intl
ms.assetid: 78da443e-ad92-4e2f-aebe-c0aed880b8b6
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SORTIDFROMLCID, SORTIDFROMLCID macro [Internationalization for Windows Applications], _win32_SORTIDFROMLCID, intl.sortidfromlcid, winnt/SORTIDFROMLCID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: winnt.h
req.include-header: Windows.h
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
req.typenames: TRANSACTION_OUTCOME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnt.h
api_name:
-	SORTIDFROMLCID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SORTIDFROMLCID macro


## -description


Retrieves a <a href="https://msdn.microsoft.com/abef64b5-ca3f-4cb3-92f0-1b7286bfb686">sort order identifier</a> from a <a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">locale identifier</a>.


## -parameters




### -param lcid

Locale identifier. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

<ul>
<li>
<a href="https://msdn.microsoft.com/d37df17d-8cd5-4481-bee2-062cf9d78e9b">LOCALE_INVARIANT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/57de328c-3afc-4fbb-882c-fa35d3552c13">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9ccb489b-24d0-42e5-a01a-2cdb7c3267eb">LOCALE_USER_DEFAULT</a>
</li>
</ul>
<b>Windows Vista and later:</b> The following custom locale identifiers are also supported.

<ul>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UI_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UNSPECIFIED</a>
</li>
</ul>

## -see-also




<a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a>



<a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/45440464-0628-473b-861a-e8be7452700c">National Language Support Macros</a>



<a href="https://msdn.microsoft.com/e463a2dc-bf36-4fbb-8df6-799ca1d549fa">PRIMARYLANGID</a>



<a href="https://msdn.microsoft.com/0441c915-f910-4ac7-ac0a-0b113f490d40">SUBLANGID</a>
 

 

