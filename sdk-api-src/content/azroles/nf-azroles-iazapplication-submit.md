---
UID: NF:azroles.IAzApplication.Submit
title: IAzApplication::Submit (azroles.h)
description: Persists changes made to the IAzApplication object.helpviewer_keywords: ["AzApplication object [Security]","Submit method","IAzApplication interface [Security]","Submit method","IAzApplication.Submit","IAzApplication::Submit","Submit","Submit method [Security]","Submit method [Security]","AzApplication object","Submit method [Security]","IAzApplication interface","azroles/IAzApplication::Submit","security.iazapplication_submit"]
old-location: security\iazapplication_submit.htm
tech.root: SecAuthZ
ms.assetid: d00d55a1-884f-46c2-b80b-f90ce8f5c648
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],Submit method, IAzApplication interface [Security],Submit method, IAzApplication.Submit, IAzApplication::Submit, Submit, Submit method [Security], Submit method [Security],AzApplication object, Submit method [Security],IAzApplication interface, azroles/IAzApplication::Submit, security.iazapplication_submit
f1_keywords:
- azroles/IAzApplication.Submit
dev_langs:
- c++
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
- IAzApplication.Submit
- AzApplication.Submit
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzApplication::Submit


## -description


The <b>Submit</b> method persists changes made to the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.


## -parameters




### -param lFlags [in]

Flags that modify the behavior of the <b>Submit</b> method. The default value is zero. If the AZ_SUBMIT_FLAG_ABORT flag is specified, the changes to the object are discarded and the object is updated to match the underlying policy store.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Any additions or modifications to an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object are not persisted until the <b>Submit</b> method is called. 

The <b>Submit</b> method does not extend to child objects; child objects  must be individually persisted to the policy store. A created <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object must be submitted before it can be referenced or become a parent object. The destructor for an object silently discards unsubmitted changes.



