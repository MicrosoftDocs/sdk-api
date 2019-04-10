---
UID: NF:authz.AuthzModifySids
title: AuthzModifySids function (authz.h)
author: windows-sdk-content
description: Adds, deletes, or modifies user and device groups in the Authz client context.
old-location: security\authzmodifysids.htm
tech.root: SecAuthZ
ms.assetid: 740569A5-6159-409B-B8CB-B3A8BAE4F398
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AuthzModifySids, AuthzModifySids function [Security], authz/AuthzModifySids, security.authzmodifysids
ms.topic: function
req.header: authz.h
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
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzModifySids
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

A pointer to a <a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a> structure that specifies the groups to modify.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <a href="https://msdn.microsoft.com/C312BE7D-DA1B-47FE-80BA-7506B9A26E9E">AUTHZ_SID_OPERATION</a> enumeration must have only one element if the value of that element is AUTHZ_SID_OPERATION_REPLACE_ALL. Otherwise, the array has the same number of elements as the corresponding 
PTOKEN_GROUPS.


When you want to use <b>AuthzModifySids</b> to delete, the SIDs are matched but not the SID flags. If no matching SID is found, no modifications are done and the call fails.



