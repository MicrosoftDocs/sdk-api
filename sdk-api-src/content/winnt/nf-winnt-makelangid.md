---
UID: NF:winnt.MAKELANGID
title: MAKELANGID macro
author: windows-sdk-content
description: Creates a language identifier from a primary language identifier and a sublanguage identifier.
old-location: intl\makelangid.htm
old-project: Intl
ms.assetid: cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: MAKELANGID, MAKELANGID macro [Internationalization for Windows Applications], _win32_MAKELANGID, intl.makelangid, winnt/MAKELANGID
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
 - MAKELANGID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# MAKELANGID macro


## -description


Creates a <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> from a primary language identifier and a sublanguage identifier.


## -parameters




### -param p

TBD


### -param s

TBD






#### - usPrimaryLanguage

Primary language identifier. This identifier can be a predefined value or a value for a user-defined primary language. For a user-defined language, the identifier is a value in the range 0x0200 to 0x03FF. All other values are reserved for operating system use. For more information, see <a href="https://msdn.microsoft.com/8a6373e0-46c2-4b1b-bc67-543f426ef15a">Language Identifier Constants and Strings</a>.


#### - usSubLanguage

Sublanguage identifier. This parameter can be a predefined sublanguage identifier or a user-defined sublanguage. For a user-defined sublanguage, the identifier is a value in the range 0x20 to 0x3F. All other values are reserved for operating system use. For more information, see <a href="https://msdn.microsoft.com/8a6373e0-46c2-4b1b-bc67-543f426ef15a">Language Identifier Constants and Strings</a>.


## -remarks



The following table shows combinations of <i>usPrimaryLanguage</i> and <i>usSubLanguage</i> that have special meaning.

<table>
<tr>
<th>Primary language identifier</th>
<th>Sublanguage identifier</th>
<th>Meaning</th>
</tr>
<tr>
<td>LANG_NEUTRAL</td>
<td>SUBLANG_NEUTRAL</td>
<td>Language neutral</td>
</tr>
<tr>
<td>LANG_NEUTRAL</td>
<td>SUBLANG_DEFAULT</td>
<td>User default language</td>
</tr>
<tr>
<td>LANG_NEUTRAL</td>
<td>SUBLANG_SYS_DEFAULT</td>
<td>System default language</td>
</tr>
<tr>
<td>LANG_NEUTRAL</td>
<td>SUBLANG_CUSTOM_DEFAULT</td>
<td><b>Windows Vista and later:</b> Default custom locale</td>
</tr>
<tr>
<td>LANG_NEUTRAL</td>
<td>SUBLANG_CUSTOM_UNSPECIFIED</td>
<td><b>Windows Vista and later:</b> Unspecified custom locale</td>
</tr>
<tr>
<td>LANG_NEUTRAL</td>
<td>SUBLANG_UI_CUSTOM_DEFAULT</td>
<td><b>Windows Vista and later:</b> Default custom Multilingual User Interface locale</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e6341460-3c4e-4040-8b49-3eb7d279e571">EnumSystemLocales</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/45440464-0628-473b-861a-e8be7452700c">National Language Support Macros</a>



<a href="https://msdn.microsoft.com/e463a2dc-bf36-4fbb-8df6-799ca1d549fa">PRIMARYLANGID</a>



<a href="https://msdn.microsoft.com/0441c915-f910-4ac7-ac0a-0b113f490d40">SUBLANGID</a>
 

 

