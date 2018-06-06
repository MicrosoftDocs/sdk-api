---
UID: NF:xenroll.ICEnroll.freeRequestInfo
title: ICEnroll::freeRequestInfo
author: windows-sdk-content
description: Releases session identifiers when they are no longer needed.
old-location: security\icenroll4_freerequestinfo.htm
old-project: SecCrypto
ms.assetid: 2d3fd4d4-779f-4e28-9b07-4de17262ac5e
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CEnroll object [Security],freeRequestInfo method, ICEnroll interface [Security],freeRequestInfo method, ICEnroll.freeRequestInfo, ICEnroll2 interface [Security],freeRequestInfo method, ICEnroll2::freeRequestInfo, ICEnroll3 interface [Security],freeRequestInfo method, ICEnroll3::freeRequestInfo, ICEnroll4 interface [Security],freeRequestInfo method, ICEnroll4::freeRequestInfo, ICEnroll::freeRequestInfo, freeRequestInfo, freeRequestInfo method [Security], freeRequestInfo method [Security],CEnroll object, freeRequestInfo method [Security],ICEnroll interface, freeRequestInfo method [Security],ICEnroll2 interface, freeRequestInfo method [Security],ICEnroll3 interface, freeRequestInfo method [Security],ICEnroll4 interface, security.icenroll4_freerequestinfo, xenroll/ICEnroll2::freeRequestInfo, xenroll/ICEnroll3::freeRequestInfo, xenroll/ICEnroll4::freeRequestInfo, xenroll/ICEnroll::freeRequestInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xenroll.h
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
tech.root: 
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.freeRequestInfo
 - ICEnroll3.freeRequestInfo
 - ICEnroll2.freeRequestInfo
 - ICEnroll.freeRequestInfo
 - CEnroll.freeRequestInfo
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# ICEnroll::freeRequestInfo


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>freeRequestInfo</b> method releases session identifiers when they are no longer needed. This method was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.


## -parameters




### -param PKCS7OrPKCS10 [in]

Specifies the session identifier that represents the data.


## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>



<a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>
 

 

