---
UID: NF:azroles.IAzApplication.OpenTask
title: IAzApplication::OpenTask (azroles.h)

description: Opens an IAzTask object with the specified name.
old-location: security\iazapplication_opentask.htm
tech.root: SecAuthZ
ms.assetid: 2d34a56d-ada8-4d7d-b026-4f1abfa290ac

ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],OpenTask method, IAzApplication interface [Security],OpenTask method, IAzApplication.OpenTask, IAzApplication::OpenTask, OpenTask, OpenTask method [Security], OpenTask method [Security],AzApplication object, OpenTask method [Security],IAzApplication interface, azroles/IAzApplication::OpenTask, security.iazapplication_opentask
ms.topic: method
f1_keywords: 
 - "azroles/IAzApplication.OpenTask"
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
 - IAzApplication.OpenTask
 - AzApplication.OpenTask
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzApplication::OpenTask


## -description


The <b>OpenTask</b> method opens an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object with the specified name.


## -parameters




### -param bstrTaskName [in]

Name of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object to open.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppTask [out]

A pointer to a pointer to the opened <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.



