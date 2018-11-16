---
UID: NF:azroles.IAzApplication.OpenScope
title: IAzApplication::OpenScope
author: windows-sdk-content
description: Opens an IAzScope object with the specified name.
old-location: security\iazapplication_openscope.htm
tech.root: SecAuthZ
ms.assetid: c2959a6c-5c87-495b-8025-c6b9c330a0bc
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AzApplication object [Security],OpenScope method, IAzApplication interface [Security],OpenScope method, IAzApplication.OpenScope, IAzApplication::OpenScope, OpenScope, OpenScope method [Security], OpenScope method [Security],AzApplication object, OpenScope method [Security],IAzApplication interface, azroles/IAzApplication::OpenScope, security.iazapplication_openscope
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
 - IAzApplication.OpenScope
 - AzApplication.OpenScope
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
- apiref
: 
- COM
: 
- azroles.h
: 
- IAzApplication.OpenScope
: 
---

# IAzApplication::OpenScope


## -description


The <b>OpenScope</b> method opens an <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object with the specified name.


## -parameters




### -param bstrScopeName [in]

Name of the <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object to open.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppScope [out]

A pointer to a pointer to the opened <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.



