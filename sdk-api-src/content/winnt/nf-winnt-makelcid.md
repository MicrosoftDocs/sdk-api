---
UID: NF:winnt.MAKELCID
title: MAKELCID macro
author: windows-sdk-content
description: Creates a locale identifier from a language identifier and a sort order identifier.
old-location: intl\makelcid.htm
tech.root: Intl
ms.assetid: 2f8893a0-f916-4a62-a423-e525cf281fa4
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: MAKELCID, MAKELCID macro [Internationalization for Windows Applications], _win32_MAKELCID, intl.makelcid, winnt/MAKELCID
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - MAKELCID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MAKELCID macro


## -description


Creates a <a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">locale identifier</a> from a <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> and a <a href="https://msdn.microsoft.com/abef64b5-ca3f-4cb3-92f0-1b7286bfb686">sort order identifier</a>.


## -parameters




### -param lgid

Language identifier. This identifier is a combination of a primary language identifier and a sublanguage identifier and is usually created by using the <a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a> macro.


### -param srtid

Sort order identifier.


## -see-also




<a href="https://msdn.microsoft.com/23392f93-8724-4b58-879e-4f48aaba4084">LANGIDFROMLCID</a>



<a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/45440464-0628-473b-861a-e8be7452700c">National Language Support Macros</a>



<a href="https://msdn.microsoft.com/78da443e-ad92-4e2f-aebe-c0aed880b8b6">SORTIDFROMLCID</a>
 

 

