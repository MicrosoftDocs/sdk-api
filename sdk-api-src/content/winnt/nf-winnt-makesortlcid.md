---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MAKESORTLCID macro


## -description


Constructs a <a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">locale identifier</a> (LCID) from a <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a>, a <a href="https://msdn.microsoft.com/abef64b5-ca3f-4cb3-92f0-1b7286bfb686">sort order identifier</a>, and the sort version.


## -parameters




### -param lgid

TBD


### -param srtid

TBD


### -param ver

TBD






#### - wLanguageID

Language identifier. This parameter is a combination of a primary language identifier and a sublanguage identifier and is usually created by using the <a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a> macro.


#### - wSortID

Sort order identifier.


#### - wSortVersion

Reserved; must be 0.


## -remarks




<a href="https://msdn.microsoft.com/d37df17d-8cd5-4481-bee2-062cf9d78e9b">LOCALE_INVARIANT</a> represents a special locale-independent locale identifier. It is designed for system-level functions that require consistent results regardless of the locale that the user has chosen, for example, sorting in the file system. Typically, an application does not use LOCALE_INVARIANT because it expects the results of an action to depend on the rules governing each individual locale.


<a href="https://msdn.microsoft.com/d37df17d-8cd5-4481-bee2-062cf9d78e9b">LOCALE_INVARIANT</a> is composed of a language identifier consisting of LANG_INVARIANT for the primary language and SUBLANG_NEUTRAL for the sublanguage. SORT_DEFAULT is used for the sort order identifier.




## -see-also




<a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/45440464-0628-473b-861a-e8be7452700c">National Language Support Macros</a>
 

 

