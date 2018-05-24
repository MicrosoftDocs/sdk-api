---
UID: NS:scesvc._SCESVC_CALLBACK_INFO_
title: "_SCESVC_CALLBACK_INFO_"
author: windows-driver-content
description: The SCESVC_CALLBACK_INFO structure contains an opaque database handle and callback function pointers to query, set, and free information.
old-location: security\scesvc_callback_info.htm
old-project: SecMgmt
ms.assetid: ff232f21-2c2f-4e5e-8b2d-e89147e2d38a
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: "*PSCESVC_CALLBACK_INFO, PSCESVC_CALLBACK_INFO, PSCESVC_CALLBACK_INFO structure pointer [Security], SCESVC_CALLBACK_INFO, SCESVC_CALLBACK_INFO structure [Security], _SCESVC_CALLBACK_INFO_, _config_scesvc_callback_info, scesvc/PSCESVC_CALLBACK_INFO, scesvc/SCESVC_CALLBACK_INFO, security.scesvc_callback_info"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: scesvc.h
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
req.typenames: SCESVC_CALLBACK_INFO, *PSCESVC_CALLBACK_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Scesvc.h
api_name:
-	SCESVC_CALLBACK_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _SCESVC_CALLBACK_INFO_ structure


## -description


The <b>SCESVC_CALLBACK_INFO</b> structure contains an opaque database handle and callback function pointers to query, set, and free information.


## -struct-fields




### -field sceHandle

Specifies the opaque handle passed to the attachment by the Security Configuration tool set. This handle is used by support functions to read information from and write information to the security database.


### -field pfQueryInfo

Pointer to a 
<a href="https://msdn.microsoft.com/a0e4a205-46d4-47c9-97cf-66f6bec34a1b">PFSCE_QUERY_INFO</a> callback function that queries information in the security database.


### -field pfSetInfo

Pointer to a 
<a href="https://msdn.microsoft.com/131585a9-b0a9-4686-84ba-237bcdcc4f5f">PFSCE_SET_INFO</a> callback function that sets information in the security database.


### -field pfFreeInfo

Pointer to a 
<a href="https://msdn.microsoft.com/e7cafdbc-9ca2-4bb1-b8ed-d5553acaf7bc">PFSCE_FREE_INFO</a> callback function that frees information in the security database.


### -field pfLogInfo

Pointer to a 
<a href="https://msdn.microsoft.com/8960b0c0-abde-4ea1-bbe4-7409a848d81b">PFSCE_LOG_INFO</a> callback function that logs messages to the configuration log file or analysis log file.


## -see-also




<a href="https://msdn.microsoft.com/8db91e6f-b31e-40c6-a158-b4b3b00ba0c0">SCE_HANDLE</a>
 

 

