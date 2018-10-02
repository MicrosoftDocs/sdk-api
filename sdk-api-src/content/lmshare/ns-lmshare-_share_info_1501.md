---
UID: NS:lmshare._SHARE_INFO_1501
title: "_SHARE_INFO_1501"
author: windows-sdk-content
description: Contains the security descriptor associated with the specified share. For more information, see Security Descriptors.
old-location: fs\share_info_1501_str.htm
tech.root: NetShare
ms.assetid: ef5d4936-8c0b-4a3c-b2b9-34868eb01a2e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPSHARE_INFO_1501, *PSHARE_INFO_1501, LPSHARE_INFO_1501, LPSHARE_INFO_1501 structure pointer [Files], PSHARE_INFO_1501, PSHARE_INFO_1501 structure pointer [Files], SHARE_INFO_1501, SHARE_INFO_1501 structure [Files], _SHARE_INFO_1501, _win32_share_info_1501_str, fs.share_info_1501_str, lmshare/LPSHARE_INFO_1501, lmshare/PSHARE_INFO_1501, lmshare/SHARE_INFO_1501, netmgmt.share_info_1501_str"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmshare.h
api_name:
 - SHARE_INFO_1501
product: Windows
targetos: Windows
req.typenames: SHARE_INFO_1501, *PSHARE_INFO_1501, *LPSHARE_INFO_1501
req.redist: 
---

# _SHARE_INFO_1501 structure


## -description


Contains the security descriptor associated with the specified share. For more information, see <a href="https://msdn.microsoft.com/4ab0e7b1-1b44-4368-b2bd-106c9d2c652c">Security Descriptors</a>.


## -struct-fields




### -field shi1501_reserved

Reserved; must be zero.


### -field shi1501_security_descriptor

Specifies the 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> associated with the share.


## -see-also




<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/14886bb0-e597-4728-a64f-bc16e82874da">Network Share Functions</a>
 

 

