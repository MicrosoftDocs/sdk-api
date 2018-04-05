---
UID: NS:winhttp.__unnamed_struct_1
title: HTTP_VERSION_INFO
author: windows-driver-content
description: The HTTP_VERSION_INFO structure contains the global HTTP version.
old-location: http\http_version_info.htm
old-project: WinHttp
ms.assetid: 2d794a99-7bd2-43ad-b826-f160bf78ccac
ms.author: windowsdriverdev
ms.date: 3/8/2018
ms.keywords: "*LPHTTP_VERSION_INFO, HTTP_VERSION_INFO, HTTP_VERSION_INFO structure [HTTP], http.http_version_info, winhttp/HTTP_VERSION_INFO, winhttp_http_version_info_structure"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: HTTP_VERSION_INFO, *LPHTTP_VERSION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winhttp.h
api_name:
-	HTTP_VERSION_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# HTTP_VERSION_INFO structure


## -description


The <b>HTTP_VERSION_INFO</b> structure contains the global HTTP version.


## -struct-fields




### -field dwMajorVersion

Major version number. Must be 1. 


### -field dwMinorVersion

Minor version number. Can be either 1 or 0. 


## -remarks



<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP
		  Versions</a>
 

 

