---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __MIDL_IBackgroundCopyJob2_0005 structure


## -description


The 
<b>BG_AUTH_CREDENTIALS</b> structure identifies the target (proxy or server), authentication scheme, and the user's credentials to use for user authentication requests. The structure is passed to the 
<a href="https://msdn.microsoft.com/adaffc21-7df1-48ca-8e05-bdb09663a49b">IBackgroundCopyJob2::SetCredentials</a> method.


## -struct-fields




### -field Target

Identifies whether to use the credentials for a proxy or server authentication request. For a list of values, see the 
<a href="https://msdn.microsoft.com/efe7aa0a-48fc-4192-b81b-40d3a9b0fb22">BG_AUTH_TARGET</a> enumeration. You can specify only one value.


### -field Scheme

Identifies the scheme to use for authentication (for example, Basic or NTLM). For a list of values, see the 
<a href="https://msdn.microsoft.com/e5a97cee-0012-4e30-850a-9adc258a36d3">BG_AUTH_SCHEME</a> enumeration. You can specify only one value.


### -field Credentials

Identifies the credentials to use for the specified authentication scheme. For details, see the 
<a href="https://msdn.microsoft.com/c16c616c-f4cb-483d-8a15-6ff9d45762ae">BG_AUTH_CREDENTIALS_UNION</a> union.


## -see-also




<a href="https://msdn.microsoft.com/c16c616c-f4cb-483d-8a15-6ff9d45762ae">BG_AUTH_CREDENTIALS_UNION</a>



<a href="https://msdn.microsoft.com/e5a97cee-0012-4e30-850a-9adc258a36d3">BG_AUTH_SCHEME</a>



<a href="https://msdn.microsoft.com/efe7aa0a-48fc-4192-b81b-40d3a9b0fb22">BG_AUTH_TARGET</a>



<a href="https://msdn.microsoft.com/adaffc21-7df1-48ca-8e05-bdb09663a49b">IBackgroundCopyJob2::SetCredentials</a>
 

 

