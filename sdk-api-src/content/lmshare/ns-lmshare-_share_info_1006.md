---
UID: NS:lmshare._SHARE_INFO_1006
title: "_SHARE_INFO_1006"
author: windows-sdk-content
description: Specifies the maximum number of concurrent connections that the shared resource can accommodate.
old-location: fs\share_info_1006_str.htm
old-project: netshare
ms.assetid: 645a8670-5661-4d6c-8d9e-67c1bbb0f1d7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPSHARE_INFO_1006, *PSHARE_INFO_1006, LPSHARE_INFO_1006, LPSHARE_INFO_1006 structure pointer [Files], PSHARE_INFO_1006, PSHARE_INFO_1006 structure pointer [Files], SHARE_INFO_1006, SHARE_INFO_1006 structure [Files], _SHARE_INFO_1006, _win32_share_info_1006_str, fs.share_info_1006_str, lmshare/LPSHARE_INFO_1006, lmshare/PSHARE_INFO_1006, lmshare/SHARE_INFO_1006, netmgmt.share_info_1006_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lmshare.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: SHARE_INFO_1006, *PSHARE_INFO_1006, *LPSHARE_INFO_1006
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmshare.h
api_name:
 - SHARE_INFO_1006
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _SHARE_INFO_1006 structure


## -description


Specifies the maximum number of concurrent connections that the shared resource can accommodate.


## -struct-fields




### -field shi1006_max_uses

Specifies a DWORD value that indicates the maximum number of concurrent connections that the shared resource can accommodate. The number of connections is unlimited if the value specified in this member is –1.


## -see-also




<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/14886bb0-e597-4728-a64f-bc16e82874da">Network Share Functions</a>
 

 

