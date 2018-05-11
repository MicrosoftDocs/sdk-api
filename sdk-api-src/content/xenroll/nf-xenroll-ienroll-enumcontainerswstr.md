---
UID: NF:xenroll.IEnroll.enumContainersWStr
title: IEnroll::enumContainersWStr
author: windows-driver-content
description: Retrieves the names of containers for the cryptographic service provider (CSP) specified by the ProviderNameWStr property.
old-location: security\ienroll4_enumcontainerswstr.htm
old-project: SecCrypto
ms.assetid: a08d97c9-8ee9-464e-862e-18c335695927
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IEnroll interface [Security],enumContainersWStr method, IEnroll.enumContainersWStr, IEnroll::enumContainersWStr, enumContainersWStr, enumContainersWStr method [Security], enumContainersWStr method [Security],IEnroll interface, security.ienroll4_enumcontainerswstr, xenroll/IEnroll::enumContainersWStr
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Xenroll.dll
api_name:
-	IEnroll.enumContainersWStr
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll::enumContainersWStr


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>enumContainersWStr</b> method retrieves the names of containers for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) specified by the 
<a href="https://msdn.microsoft.com/42300501-2a64-4433-81e9-6ee3fc31b094">ProviderNameWStr</a> property. This method was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.


## -parameters




### -param dwIndex [in]

Specifies the ordinal position of the container whose name will be retrieved. Specify zero for the first container.


### -param pbstr






#### - ppwsz [out]

A pointer to a <b>LPWSTR</b> variable that receives the name of the container.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. The value ERROR_NO_MORE_ITEMS is returned when there are no more items.




## -remarks



If the 
<a href="https://msdn.microsoft.com/42300501-2a64-4433-81e9-6ee3fc31b094">ProviderNameWStr</a> property value has not been set, the default value (usually Microsoft Base Cryptographic Provider) of <b>ProviderNameWStr</b> as set in the registry is used.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 

