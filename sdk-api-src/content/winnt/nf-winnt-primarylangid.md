---
UID: NF:winnt.PRIMARYLANGID
title: PRIMARYLANGID macro (winnt.h)
author: windows-sdk-content
description: Extracts a primary language identifier from a language identifier.
old-location: intl\primarylangid.htm
tech.root: Intl
ms.assetid: e463a2dc-bf36-4fbb-8df6-799ca1d549fa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PRIMARYLANGID, PRIMARYLANGID macro [Internationalization for Windows Applications], _win32_PRIMARYLANGID, intl.primarylangid, winnt/PRIMARYLANGID
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
 - PRIMARYLANGID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PRIMARYLANGID macro


## -description


Extracts a primary language identifier from a <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a>.


## -parameters




### -param lgid

Language identifier. This value is a combination of a primary language identifier and a sublanguage identifier and is usually created by using the <a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a> macro.


## -see-also




<a href="https://msdn.microsoft.com/e6341460-3c4e-4040-8b49-3eb7d279e571">EnumSystemLocales</a>



<a href="https://msdn.microsoft.com/23392f93-8724-4b58-879e-4f48aaba4084">LANGIDFROMLCID</a>



<a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/45440464-0628-473b-861a-e8be7452700c">National Language Support Macros</a>



<a href="https://msdn.microsoft.com/0441c915-f910-4ac7-ac0a-0b113f490d40">SUBLANGID</a>
 

 

