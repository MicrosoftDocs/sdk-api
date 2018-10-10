---
UID: NS:winnetwk._UNIVERSAL_NAME_INFOW
title: "_UNIVERSAL_NAME_INFOW"
author: windows-sdk-content
description: The UNIVERSAL_NAME_INFO structure contains a pointer to a Universal Naming Convention (UNC) name string for a network resource.
old-location: wnet\universal_name_info_str.htm
tech.root: WNet
ms.assetid: 36e64c8a-595a-4d41-aa83-592d525c98ee
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPUNIVERSAL_NAME_INFOW, UNIVERSAL_NAME_INFO, UNIVERSAL_NAME_INFO structure [Windows Networking (WNet)], UNIVERSAL_NAME_INFOA, UNIVERSAL_NAME_INFOW, _UNIVERSAL_NAME_INFOA, _UNIVERSAL_NAME_INFOW, _win32_universal_name_info_str, winnetwk/UNIVERSAL_NAME_INFO, winnetwk/_UNIVERSAL_NAME_INFOA, winnetwk/_UNIVERSAL_NAME_INFOW, wnet.universal_name_info_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: "_UNIVERSAL_NAME_INFOW (Unicode) and _UNIVERSAL_NAME_INFOA (ANSI)"
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
 - Winnetwk.h
api_name:
 - UNIVERSAL_NAME_INFO
 - _UNIVERSAL_NAME_INFOA
 - _UNIVERSAL_NAME_INFOW
product: Windows
targetos: Windows
req.typenames: UNIVERSAL_NAME_INFOW, *LPUNIVERSAL_NAME_INFOW
req.redist: 
---

# _UNIVERSAL_NAME_INFOW structure


## -description


The
				<b>UNIVERSAL_NAME_INFO</b> structure contains a pointer to a Universal Naming Convention (UNC) name string for a network resource.


## -struct-fields




### -field lpUniversalName

Pointer to the null-terminated UNC name string that identifies a network resource.


## -remarks



A UNC path identifies a network resource in an unambiguous, computer-independent manner. You can pass the path to processes on other computers, allowing those processes to obtain access to the network resource.

Universal Naming Convention (UNC) names look like this:

<pre class="syntax" xml:space="preserve"><code>\\servername\sharename\path\file
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/0cc2ae86-8a46-4e1b-8c28-5904486ffcb5">REMOTE_NAME_INFO</a>



<a href="https://msdn.microsoft.com/12c02092-f2d5-4477-92a7-ae075b8a243a">WNetGetUniversalName</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/7969ccbb-d1ae-4a1f-8b9c-862cc6ddef1a">Windows Networking Structures</a>
 

 

