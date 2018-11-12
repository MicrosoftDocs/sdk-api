---
UID: NS:wincrypt._CROSS_CERT_DIST_POINTS_INFO
title: "_CROSS_CERT_DIST_POINTS_INFO"
author: windows-sdk-content
description: Provides information used to update dynamic cross certificates.
old-location: security\cross_cert_dist_points_info.htm
tech.root: seccrypto
ms.assetid: 13358822-c690-40af-ba9d-2fafa0233a5c
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*PCROSS_CERT_DIST_POINTS_INFO, CROSS_CERT_DIST_POINTS_INFO, CROSS_CERT_DIST_POINTS_INFO structure [Security], PCROSS_CERT_DIST_POINTS_INFO, PCROSS_CERT_DIST_POINTS_INFO structure pointer [Security], _CROSS_CERT_DIST_POINTS_INFO, _crypto2_cross_cert_dist_points_info, security.cross_cert_dist_points_info, wincrypt/CROSS_CERT_DIST_POINTS_INFO, wincrypt/PCROSS_CERT_DIST_POINTS_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
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
 - Wincrypt.h
api_name:
 - CROSS_CERT_DIST_POINTS_INFO
product: Windows
targetos: Windows
req.typenames: CROSS_CERT_DIST_POINTS_INFO, *PCROSS_CERT_DIST_POINTS_INFO
req.redist: 
---

# _CROSS_CERT_DIST_POINTS_INFO structure


## -description


The <b>CROSS_CERT_DIST_POINTS_INFO</b> structure provides information used to update dynamic cross certificates.


## -struct-fields




### -field dwSyncDeltaTime

<b>DWORD</b> indicating seconds between synchronization. If this member is zero, the client default synchronization time is used.


### -field cDistPoint

Count of the number of elements in the <b>rgDistPoint</b> member array.


### -field rgDistPoint

Array of 
<a href="https://msdn.microsoft.com/f9a20827-3333-4ce2-b074-2e8ce903fad2">CERT_ALT_NAME_INFO</a> structures for distribution points for updating cross certificates.

