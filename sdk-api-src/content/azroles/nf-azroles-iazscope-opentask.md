---
UID: NF:azroles.IAzScope.OpenTask
title: IAzScope::OpenTask
author: windows-sdk-content
description: Opens an IAzTask object with the specified name.
old-location: security\iazscope_opentask.htm
old-project: SecAuthZ
ms.assetid: 8719ab1f-8004-4d5c-b64c-ae17c8d1ab30
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AzScope object [Security],OpenTask method, IAzScope interface [Security],OpenTask method, IAzScope.OpenTask, IAzScope::OpenTask, OpenTask, OpenTask method [Security], OpenTask method [Security],AzScope object, OpenTask method [Security],IAzScope interface, azroles/IAzScope::OpenTask, security.iazscope_opentask
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
-	IAzScope.OpenTask
-	AzScope.OpenTask
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzScope::OpenTask


## -description


The <b>OpenTask</b> method opens an <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object with the specified name.


## -parameters




### -param bstrTaskName [in]

Name of the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object to open.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppTask [out]

A pointer to a pointer to the opened <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.



