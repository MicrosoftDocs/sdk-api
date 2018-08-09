---
UID: NF:winnt.MAKESORTLCID
title: MAKESORTLCID macro
author: windows-sdk-content
description: Constructs a locale identifier (LCID) from a language identifier, a sort order identifier, and the sort version.
old-location: intl\makesortlcid.htm
old-project: Intl
ms.assetid: 58327bfc-8a00-4fdc-bd5a-cef9c0b29faa
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MAKESORTLCID, MAKESORTLCID macro [Internationalization for Windows Applications], _win32_MAKESORTLCID, intl.makesortlcid, winnt/MAKESORTLCID
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
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - MAKESORTLCID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# MAKESORTLCID macro


## -description


Constructs a <a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">locale identifier</a> (LCID) from a <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a>, a <a href="https://msdn.microsoft.com/abef64b5-ca3f-4cb3-92f0-1b7286bfb686">sort order identifier</a>, and the sort version.


## -parameters




### -param lgid

Language identifier. This parameter is a combination of a primary language identifier and a sublanguage identifier and is usually created by using the <a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a> macro.


### -param srtid

Sort order identifier.


### -param ver

Reserved; must be 0.


## -remarks




<a href="https://msdn.microsoft.com/d37df17d-8cd5-4481-bee2-062cf9d78e9b">LOCALE_INVARIANT</a> represents a special locale-independent locale identifier. It is designed for system-level functions that require consistent results regardless of the locale that the user has chosen, for example, sorting in the file system. Typically, an application does not use LOCALE_INVARIANT because it expects the results of an action to depend on the rules governing each individual locale.


<a href="https://msdn.microsoft.com/d37df17d-8cd5-4481-bee2-062cf9d78e9b">LOCALE_INVARIANT</a> is composed of a language identifier consisting of LANG_INVARIANT for the primary language and SUBLANG_NEUTRAL for the sublanguage. SORT_DEFAULT is used for the sort order identifier.




## -see-also




<a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/45440464-0628-473b-861a-e8be7452700c">National Language Support Macros</a>
 

 

