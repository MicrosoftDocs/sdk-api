---
UID: NF:azroles.IAzAuthorizationStore3.IsUpdateNeeded
title: IAzAuthorizationStore3::IsUpdateNeeded (azroles.h)
author: windows-sdk-content
description: Checks whether the persisted version of this authorization store is newer than the cached version.
old-location: security\iazauthorizationstore3_isupdateneeded_method.htm
tech.root: SecAuthZ
ms.assetid: 2b5bed8f-f38a-46dd-b889-65d43b13ce7c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAzAuthorizationStore3 interface [Security],IsUpdateNeeded method, IAzAuthorizationStore3.IsUpdateNeeded, IAzAuthorizationStore3::IsUpdateNeeded, IsUpdateNeeded, IsUpdateNeeded method [Security], IsUpdateNeeded method [Security],IAzAuthorizationStore3 interface, azroles/IAzAuthorizationStore3::IsUpdateNeeded, security.iazauthorizationstore3_isupdateneeded_method
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Azroles.idl
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
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzAuthorizationStore3.IsUpdateNeeded
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzAuthorizationStore3::IsUpdateNeeded


## -description


The <b>IsUpdateNeeded</b> method checks whether the persisted version of this authorization store is newer than the cached version. If the cached version of the store is newer, the calling application can update the cached version by calling the <a href="https://msdn.microsoft.com/1fd17040-f736-44a6-8a01-720f4c8fe9ac">UpdateCache</a> method of the <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object.


## -parameters




### -param pbIsUpdateNeeded [out]

<b>VARIANT_TRUE</b> if the persisted version of this authorization store is newer than the cached version; otherwise, <b>VARIANT_FALSE</b>.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



