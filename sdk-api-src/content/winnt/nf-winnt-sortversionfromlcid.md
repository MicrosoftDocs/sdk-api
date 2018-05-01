---
UID: NF:winnt.SORTVERSIONFROMLCID
title: SORTVERSIONFROMLCID macro
author: windows-driver-content
description: Retrieves the sort version from a locale identifier.
old-location: intl\sortversionfromlcid.htm
old-project: Intl
ms.assetid: 2a851ec1-ccb9-42d3-bbb5-70cb9cf02cc7
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: SORTVERSIONFROMLCID, SORTVERSIONFROMLCID macro [Internationalization for Windows Applications], _win32_SORTVERSIONFROMLCID, intl.sortversionfromlcid, winnt/SORTVERSIONFROMLCID
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TRANSACTION_OUTCOME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnt.h
api_name:
-	SORTVERSIONFROMLCID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SORTVERSIONFROMLCID macro


## -description


Retrieves the sort version from a <a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">locale identifier</a>.


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

## -remarks



Note that this macro is entirely distinct from <a href="https://msdn.microsoft.com/78da443e-ad92-4e2f-aebe-c0aed880b8b6">SORTIDFROMLCID</a>.




## -see-also




<a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/45440464-0628-473b-861a-e8be7452700c">National Language Support Macros</a>



<a href="https://msdn.microsoft.com/78da443e-ad92-4e2f-aebe-c0aed880b8b6">SORTIDFROMLCID</a>
 

 

