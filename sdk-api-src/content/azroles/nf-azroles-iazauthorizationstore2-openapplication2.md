---
UID: NF:azroles.IAzAuthorizationStore2.OpenApplication2
title: IAzAuthorizationStore2::OpenApplication2
author: windows-sdk-content
description: Opens the IAzApplication2 object with the specified name.
old-location: security\iazauthorizationstore2_openapplication2.htm
old-project: secauthz
ms.assetid: 8705ea59-2419-4af5-9cc2-591221e09073
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: IAzAuthorizationStore2 interface [Security],OpenApplication2 method, IAzAuthorizationStore2.OpenApplication2, IAzAuthorizationStore2::OpenApplication2, OpenApplication2, OpenApplication2 method [Security], OpenApplication2 method [Security],IAzAuthorizationStore2 interface, azroles/IAzAuthorizationStore2::OpenApplication2, security.iazauthorizationstore2_openapplication2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzAuthorizationStore2.OpenApplication2
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore2::OpenApplication2


## -description


The <b>OpenApplication2</b> method opens the <a href="https://msdn.microsoft.com/58f0627e-fa92-4b3b-a0cd-7e437d451606">IAzApplication2</a> object with the specified name.


## -parameters




### -param bstrApplicationName [in]

The name of the <a href="https://msdn.microsoft.com/58f0627e-fa92-4b3b-a0cd-7e437d451606">IAzApplication2</a> object to open.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppApplication [out]

A pointer to a pointer to the opened <a href="https://msdn.microsoft.com/58f0627e-fa92-4b3b-a0cd-7e437d451606">IAzApplication2</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



