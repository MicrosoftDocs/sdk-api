---
UID: NF:azroles.IAzApplication.CreateScope
title: IAzApplication::CreateScope
author: windows-driver-content
description: Creates an IAzScope object with the specified name.
old-location: security\iazapplication_createscope.htm
old-project: SecAuthZ
ms.assetid: 6d5044d8-0b6a-4681-a8eb-e93f50fbdf36
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AzApplication object [Security],CreateScope method, CreateScope, CreateScope method [Security], CreateScope method [Security],AzApplication object, CreateScope method [Security],IAzApplication interface, IAzApplication interface [Security],CreateScope method, IAzApplication.CreateScope, IAzApplication::CreateScope, azroles/IAzApplication::CreateScope, security.iazapplication_createscope
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzApplication.CreateScope
-	AzApplication.CreateScope
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::CreateScope


## -description


The <b>CreateScope</b> method creates an <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object with the specified name.


## -parameters




### -param bstrScopeName [in]

Name for the new <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppScope [out]

A pointer to a pointer to the created <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.




## -remarks



You must call the <a href="https://msdn.microsoft.com/c06f1994-71d9-4867-a5ed-8fa90206994f">IAzScope::Submit</a> method to persist any changes made to the returned object.

The returned <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object is an immediate child object of the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object.



