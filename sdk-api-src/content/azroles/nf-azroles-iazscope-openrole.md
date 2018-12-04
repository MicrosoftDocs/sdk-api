---
UID: NF:azroles.IAzScope.OpenRole
title: IAzScope::OpenRole
author: windows-sdk-content
description: Opens an IAzRole object with the specified name.
old-location: security\iazscope_openrole.htm
tech.root: secauthz
ms.assetid: 55ec166e-5aad-411d-8cc4-0d789c8397c4
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: AzScope object [Security],OpenRole method, IAzScope interface [Security],OpenRole method, IAzScope.OpenRole, IAzScope::OpenRole, OpenRole, OpenRole method [Security], OpenRole method [Security],AzScope object, OpenRole method [Security],IAzScope interface, azroles/IAzScope::OpenRole, security.iazscope_openrole
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
 - IAzScope.OpenRole
 - AzScope.OpenRole
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzScope::OpenRole


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



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.



