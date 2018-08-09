---
UID: NF:azroles.IAzScope.OpenApplicationGroup
title: IAzScope::OpenApplicationGroup
author: windows-sdk-content
description: Opens an IAzApplicationGroup object by specifying its name.
old-location: security\iazscope_openapplicationgroup.htm
old-project: secauthz
ms.assetid: 6c0e2832-e46b-428e-8f0b-ca1d816afaeb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AzScope object [Security],OpenApplicationGroup method, IAzScope interface [Security],OpenApplicationGroup method, IAzScope.OpenApplicationGroup, IAzScope::OpenApplicationGroup, OpenApplicationGroup, OpenApplicationGroup method [Security], OpenApplicationGroup method [Security],AzScope object, OpenApplicationGroup method [Security],IAzScope interface, azroles/IAzScope::OpenApplicationGroup, security.iazscope_openapplicationgroup
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
 - IAzScope.OpenApplicationGroup
 - AzScope.OpenApplicationGroup
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzScope::OpenApplicationGroup


## -description


The <b>OpenApplicationGroup</b> method opens an <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object with the specified name.


## -parameters




### -param bstrGroupName [in]

Name of the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object to open.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppGroup [out]

A pointer to a pointer to the opened <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.



