---
UID: NS:lmuse._USE_INFO_0
title: USE_INFO_0 (lmuse.h)
author: windows-sdk-content
description: The USE_INFO_0 structure contains the name of a shared resource and the local device redirected to it.
old-location: netmgmt\use_info_0_str.htm
tech.root: NetMgmt
ms.assetid: 86db3f19-84c5-4e89-82cb-f01d17dcf4ec
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPUSE_INFO_0, *PUSE_INFO_0, LPUSE_INFO_0, LPUSE_INFO_0 structure pointer [Network Management], PUSE_INFO_0, PUSE_INFO_0 structure pointer [Network Management], USE_INFO_0, USE_INFO_0 structure [Network Management], _win32_use_info_0_str, lmuse/LPUSE_INFO_0, lmuse/PUSE_INFO_0, lmuse/USE_INFO_0, netmgmt.use_info_0_str"
ms.topic: struct
req.header: lmuse.h
req.include-header: Lm.h
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
 - Lmuse.h
api_name:
 - USE_INFO_0
product: Windows
targetos: Windows
req.typenames: USE_INFO_0, *PUSE_INFO_0, *LPUSE_INFO_0
req.redist: 
---

# USE_INFO_0 structure


## -description


The
				<b>USE_INFO_0</b> structure contains the name of a shared resource and the local device redirected to it.


## -struct-fields




### -field ui0_local

Pointer to a Unicode string that specifies the local device name (for example, drive E or LPT1) being redirected to the shared resource. The constant DEVLEN specifies the maximum number of characters in the string.


### -field ui0_remote

Pointer to a Unicode string that specifies the share name of the remote resource being accessed. The string is in the form: 




<pre class="syntax" xml:space="preserve"><code>\\servername\sharename
</code></pre>

## -see-also




<a href="https://msdn.microsoft.com/fb527f85-baea-48e8-b837-967870834ec5">NetUseEnum</a>



<a href="https://msdn.microsoft.com/257875db-5ed9-4569-8dbb-5dcc7a6af95c">NetUseGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/ddf1b8dc-f13b-402a-9e4e-e4944a29ac31">Use Functions</a>
 

 

