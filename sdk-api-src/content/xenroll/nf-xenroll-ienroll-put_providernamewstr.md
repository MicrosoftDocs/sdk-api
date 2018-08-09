---
UID: NF:xenroll.IEnroll.put_ProviderNameWStr
title: IEnroll::put_ProviderNameWStr
author: windows-sdk-content
description: Sets or retrieves the name of the cryptographic service provider (CSP) to use.
old-location: security\ienroll4_providernamewstr.htm
old-project: seccrypto
ms.assetid: 42300501-2a64-4433-81e9-6ee3fc31b094
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnroll interface [Security],ProviderNameWStr property, IEnroll.ProviderNameWStr, IEnroll.put_ProviderNameWStr, IEnroll::ProviderNameWStr, IEnroll::get_ProviderNameWStr, IEnroll::put_ProviderNameWStr, ProviderNameWStr property [Security], ProviderNameWStr property [Security],IEnroll interface, put_ProviderNameWStr, security.ienroll4_providernamewstr, xenroll/IEnroll::ProviderNameWStr, xenroll/IEnroll::get_ProviderNameWStr, xenroll/IEnroll::put_ProviderNameWStr
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
 - IEnroll.ProviderNameWStr
 - IEnroll.get_ProviderNameWStr
 - IEnroll.put_ProviderNameWStr
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll::put_ProviderNameWStr


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ProviderNameWStr</b> property sets or retrieves the name of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) to use.

If the CSP has not been specified, the default value for this property  is "Microsoft Base Cryptographic Provider", and the <b>ProviderNameWStr</b> property is set to an empty string. This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks




The <b>ProviderNameWStr</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/ebbcc9ad-9f87-4abe-963b-38c57a60e45e">createPKCS10WStr</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5edd54c5-9dfb-44b8-a293-4fe6a8de45e3">createFilePKCS10WStr</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a08d97c9-8ee9-464e-862e-18c335695927">enumContainersWStr</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 

