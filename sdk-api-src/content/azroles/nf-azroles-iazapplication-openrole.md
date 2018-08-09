---
UID: NF:azroles.IAzApplication.OpenRole
title: IAzApplication::OpenRole
author: windows-sdk-content
description: Opens an IAzRole object with the specified name.
old-location: security\iazapplication_openrole.htm
old-project: secauthz
ms.assetid: 483c5b08-2f40-4ba6-afa0-ede596df8495
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AzApplication object [Security],OpenRole method, IAzApplication interface [Security],OpenRole method, IAzApplication.OpenRole, IAzApplication::OpenRole, OpenRole, OpenRole method [Security], OpenRole method [Security],AzApplication object, OpenRole method [Security],IAzApplication interface, azroles/IAzApplication::OpenRole, security.iazapplication_openrole
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication.OpenRole
 - AzApplication.OpenRole
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::OpenRole


## -description


The <b>OpenRole</b> method opens an <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object with the specified name.


## -parameters




### -param bstrRoleName [in]

Name of the <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object to open.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppRole [out]

A pointer to a pointer to the opened <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.



