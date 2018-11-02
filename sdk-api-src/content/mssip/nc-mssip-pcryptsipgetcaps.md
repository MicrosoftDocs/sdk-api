---
UID: NC:mssip.pCryptSIPGetCaps
title: pCryptSIPGetCaps
author: windows-sdk-content
description: Is implemented by an subject interface package (SIP) to report capabilities.
old-location: security\pfncryptsipgetcaps.htm
tech.root: seccrypto
ms.assetid: 8EA46B67-F542-4B15-81F4-3DD83DD45764
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: mssip/pCryptSIPGetCaps, pCryptSIPGetCaps, pCryptSIPGetCaps callback, pCryptSIPGetCaps callback function [Security], security.pfncryptsipgetcaps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: mssip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - UserDefined
api_location:
 - Mssip.h
api_name:
 - pCryptSIPGetCaps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# pCryptSIPGetCaps callback function


## -description


The <b>pCryptSIPGetCaps</b> function is implemented by an <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface package</a> (SIP) to report capabilities.


## -parameters




### -param *pSubjInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/6274cd08-d67f-410d-9303-3a42b7f1edc6">SIP_SUBJECTINFO</a> structure that specifies subject information data to the SIP APIs.


### -param *pCaps [in, out]

Pointer to a <a href="https://msdn.microsoft.com/0B6D173B-0183-4A7C-BB92-2D451F746164">SIP_CAP_SET</a> structure that defines the capabilities of an SIP.


## -see-also




<a href="https://msdn.microsoft.com/F939F6D5-DDFE-478F-8FDD-8FA9FAB26010">CryptSIPGetCaps</a>



<a href="https://msdn.microsoft.com/0B6D173B-0183-4A7C-BB92-2D451F746164">SIP_CAP_SET</a>



<a href="https://msdn.microsoft.com/6274cd08-d67f-410d-9303-3a42b7f1edc6">SIP_SUBJECTINFO</a>
 

 

