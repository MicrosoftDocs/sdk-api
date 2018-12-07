---
UID: NS:wininet.INTERNET_VERSION_INFO
title: INTERNET_VERSION_INFO
author: windows-sdk-content
description: Contains the HTTP version number of the server. This structure is used when passing the INTERNET_OPTION_VERSION flag to the InternetQueryOption function.
old-location: wininet\internet_version_info.htm
tech.root: WinInet
ms.assetid: 6d979829-2451-47fa-a95f-81f447c93567
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPINTERNET_VERSION_INFO, INTERNET_VERSION_INFO, INTERNET_VERSION_INFO structure [WinINet], LPINTERNET_VERSION_INFO, LPINTERNET_VERSION_INFO structure pointer [WinINet], _inet_internet_verion_info_structure, wininet.internet_version_info, wininet/ LPINTERNET_VERSION_INFO, wininet/INTERNET_VERSION_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wininet.h
req.include-header: 
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
 - Wininet.h
api_name:
 - INTERNET_VERSION_INFO
product: Windows
targetos: Windows
req.typenames: INTERNET_VERSION_INFO, *LPINTERNET_VERSION_INFO
req.redist: 
---

# INTERNET_VERSION_INFO structure


## -description


Contains the HTTP version number of the server. This structure is used when passing the INTERNET_OPTION_VERSION flag to the 
<a href="https://msdn.microsoft.com/b0bafd3d-8f54-429e-b423-dae3d61b0030">InternetQueryOption</a> function.


## -struct-fields




### -field dwMajorVersion

Major version number. 


### -field dwMinorVersion

Minor version number. 


## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b0bafd3d-8f54-429e-b423-dae3d61b0030">InternetQueryOption</a>
 

 

