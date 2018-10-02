---
UID: NF:azroles.IAzOperation.Submit
title: IAzOperation::Submit
author: windows-sdk-content
description: Persists changes made to the IAzOperation object.
old-location: security\iazoperation_submit.htm
tech.root: SecAuthZ
ms.assetid: f6265bfa-c856-47db-a688-f5de25ef7157
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AzOperation object [Security],Submit method, IAzOperation interface [Security],Submit method, IAzOperation.Submit, IAzOperation::Submit, Submit, Submit method [Security], Submit method [Security],AzOperation object, Submit method [Security],IAzOperation interface, azroles/IAzOperation::Submit, security.iazoperation_submit
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzOperation.Submit
 - AzOperation.Submit
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzOperation::Submit


## -description


The <b>Submit</b> method persists changes made to the <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object.


## -parameters




### -param lFlags [in, optional]

Flags that modify the behavior of the <b>Submit</b> method. The default value is zero. If the AZ_SUBMIT_FLAG_ABORT flag is specified, the changes to the object are discarded and the object is updated to match the underlying policy store.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Any additions or modifications to an <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object are not persisted until the <b>Submit</b> method is called.



