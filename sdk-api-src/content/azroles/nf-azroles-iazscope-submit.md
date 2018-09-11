---
UID: NF:azroles.IAzScope.Submit
title: IAzScope::Submit
author: windows-sdk-content
description: Persists changes made to the IAzScope object.
old-location: security\iazscope_submit.htm
tech.root: SecAuthZ
ms.assetid: c06f1994-71d9-4867-a5ed-8fa90206994f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AzScope object [Security],Submit method, IAzScope interface [Security],Submit method, IAzScope.Submit, IAzScope::Submit, Submit, Submit method [Security], Submit method [Security],AzScope object, Submit method [Security],IAzScope interface, azroles/IAzScope::Submit, security.iazscope_submit
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
 - IAzScope.Submit
 - AzScope.Submit
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzScope::Submit


## -description


The <b>Submit</b> method persists changes made to the <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object.


## -parameters




### -param lFlags [in]

Flags that modify the behavior of the <b>Submit</b> method. The default value is zero. If the AZ_SUBMIT_FLAG_ABORT flag is specified, the changes to the object are discarded and the object is updated to match the underlying policy store.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Any additions or modifications to an <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object are not persisted until the <b>Submit</b> method is called. 

The <b>Submit</b> method does not extend to child objects; child objects  must be individually persisted to the policy store. A created <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object must be submitted before it can be referenced or become a parent object. The destructor for an object silently discards unsubmitted changes.



