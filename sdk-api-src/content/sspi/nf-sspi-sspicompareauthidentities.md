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

# SspiCompareAuthIdentities function


## -description


Compares the two specified credentials.


## -parameters




### -param AuthIdentity1 [in]

A pointer to an opaque structure that specifies the first credential to compare.


### -param AuthIdentity2 [in]

A pointer to an opaque structure that specifies the second credential to compare.


### -param SameSuppliedUser [out]

<b>TRUE</b> if the user account specified by the <i>AuthIdentity1</i> parameter is the same as the user account specified by the <i>AuthIdentity2</i> parameter; otherwise, <b>FALSE</b>.


### -param SameSuppliedIdentity [out]

<b>TRUE</b> if the identity specified by the <i>AuthIdentity1</i> parameter is the same as the identity specified by the <i>AuthIdentity2</i> parameter; otherwise, <b>FALSE</b>.


## -returns




						If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



