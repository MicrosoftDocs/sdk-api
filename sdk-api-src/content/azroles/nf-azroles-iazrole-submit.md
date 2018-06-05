---
UID: NF:azroles.IAzRole.Submit
title: IAzRole::Submit
author: windows-sdk-content
description: Persists changes made to the IAzRole object.
old-location: security\iazrole_submit.htm
old-project: SecAuthZ
ms.assetid: 97f2018a-92f0-4ebb-85f1-78c140003d8f
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AzRole object [Security],Submit method, IAzRole interface [Security],Submit method, IAzRole.Submit, IAzRole::Submit, Submit, Submit method [Security], Submit method [Security],AzRole object, Submit method [Security],IAzRole interface, azroles/IAzRole::Submit, security.iazrole_submit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzRole.Submit
-	AzRole.Submit
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzRole::Submit


## -description


The <b>Submit</b> method persists changes made to the <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object.


## -parameters




### -param lFlags [in, optional]

Flags that modify the behavior of the <b>Submit</b> method. The default value is zero. If the AZ_SUBMIT_FLAG_ABORT flag is specified, the changes to the object are discarded and the object is updated to match the underlying policy store.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Any additions or modifications to an <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object are not persisted until the <b>Submit</b> method is called.



