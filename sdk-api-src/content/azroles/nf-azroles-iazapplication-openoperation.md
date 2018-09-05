---
UID: NF:azroles.IAzApplication.OpenOperation
title: IAzApplication::OpenOperation
author: windows-sdk-content
description: Opens an IAzOperation object with the specified name.
old-location: security\iazapplication_openoperation.htm
old-project: SecAuthZ
ms.assetid: 37dddf38-a79b-419f-891b-8da7dc2bdf42
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AzApplication object [Security],OpenOperation method, IAzApplication interface [Security],OpenOperation method, IAzApplication.OpenOperation, IAzApplication::OpenOperation, OpenOperation, OpenOperation method [Security], OpenOperation method [Security],AzApplication object, OpenOperation method [Security],IAzApplication interface, azroles/IAzApplication::OpenOperation, security.iazapplication_openoperation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication.OpenOperation
 - AzApplication.OpenOperation
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::OpenOperation


## -description


The <b>OpenOperation</b> method opens an <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object with the specified name.


## -parameters




### -param bstrOperationName [in]

Name of the <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object to open.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppOperation [out]

A pointer to a pointer to the opened <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.



