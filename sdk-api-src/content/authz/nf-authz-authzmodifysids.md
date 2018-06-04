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

# AuthzModifySids function


## -description


The <b>AuthzModifySids</b> function adds, deletes, or modifies user and device groups in the Authz client context.


## -parameters




### -param hAuthzClientContext [in]

A handle to the client context to be modified.


### -param SidClass [in]

Type of information to be modified. The caller can specify AuthzContextInfoGroupsSids, AuthzContextInfoRestrictedSids, or AuthzContextInfoDeviceSids.


### -param pSidOperations [in]

A pointer to an array of <a href="https://msdn.microsoft.com/C312BE7D-DA1B-47FE-80BA-7506B9A26E9E">AUTHZ_SID_OPERATION</a> enumeration values that specify the group modifications to make.


### -param pSids [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a> structure that specifies the groups to modify.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <a href="https://msdn.microsoft.com/C312BE7D-DA1B-47FE-80BA-7506B9A26E9E">AUTHZ_SID_OPERATION</a> enumeration must have only one element if the value of that element is AUTHZ_SID_OPERATION_REPLACE_ALL. Otherwise, the array has the same number of elements as the corresponding 
PTOKEN_GROUPS.


When you want to use <b>AuthzModifySids</b> to delete, the SIDs are matched but not the SID flags. If no matching SID is found, no modifications are done and the call fails.



