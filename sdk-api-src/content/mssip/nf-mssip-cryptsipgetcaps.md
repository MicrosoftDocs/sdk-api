---
UID: NF:mssip.CryptSIPGetCaps
title: CryptSIPGetCaps function (mssip.h)
author: windows-sdk-content
description: Retrieves the capabilities of a subject interface package (SIP).
old-location: security\cryptsipgetcaps.htm
tech.root: SecCrypto
ms.assetid: F939F6D5-DDFE-478F-8FDD-8FA9FAB26010
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CryptSIPGetCaps, CryptSIPGetCaps function [Security], mssip/CryptSIPGetCaps, security.cryptsipgetcaps
ms.topic: function
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptSIPGetCaps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptSIPGetCaps function


## -description


The <b>CryptSIPGetCaps</b> function retrieves the capabilities of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface package</a> (SIP).


## -parameters




### -param pSubjInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/6274cd08-d67f-410d-9303-3a42b7f1edc6">SIP_SUBJECTINFO</a> structure that specifies subject information data to the SIP APIs.


### -param pCaps [in, out]

Pointer to a <a href="https://msdn.microsoft.com/0B6D173B-0183-4A7C-BB92-2D451F746164">SIP_CAP_SET</a> structure that defines the capabilities of an SIP.


## -remarks



Unlike other SIP functions, <b>CryptSIPGetCaps</b> is not registered in the dispatch table. For more information, see the <a href="https://msdn.microsoft.com/d34b5081-0af8-4dcc-8133-a91d0603d419">SIP_DISPATCH_INFO</a> structure. Instead, callers must map the object identifier (OID) to the function entry point. 




## -see-also




<a href="https://msdn.microsoft.com/0B6D173B-0183-4A7C-BB92-2D451F746164">SIP_CAP_SET</a>



<a href="https://msdn.microsoft.com/6274cd08-d67f-410d-9303-3a42b7f1edc6">SIP_SUBJECTINFO</a>



<a href="https://msdn.microsoft.com/8EA46B67-F542-4B15-81F4-3DD83DD45764">pCryptSIPGetCaps</a>
 

 

