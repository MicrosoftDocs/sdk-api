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

# LSA_EXPAND_AUTH_DATA_FOR_DOMAIN callback function


## -description


Expands the domain groups in the specified user authentication data.


## -parameters




### -param UserAuthData [in]

A pointer to the user authentication data to expand.


### -param UserAuthDataSize [in]

The size, in bytes, of the <i>UserAuthData</i> buffer.


### -param Reserved [in]

Reserved. This parameter must be set to <b>NULL.</b>


### -param *ExpandedAuthData [out]

A pointer to the expanded authentication data.


### -param ExpandedAuthDataSize [out]

A pointer to the size, in bytes, of the <i>ExpandedAuthData</i> buffer.


## -returns



If the function succeeds, return STATUS_SUCCESS, or an informational status code.

If the function fails, return an NTSTATUS error code that indicates the reason it failed.




## -remarks



A pointer to the <b>ExpandAuthDataForDomain</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

