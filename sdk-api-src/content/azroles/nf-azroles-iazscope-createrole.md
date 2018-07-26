---
UID: NF:azroles.IAzScope.CreateRole
title: IAzScope::CreateRole
author: windows-sdk-content
description: Creates an IAzRole object with the specified name.
old-location: security\iazscope_createrole.htm
old-project: secauthz
ms.assetid: a5e527f9-0aab-40d9-83fe-f19f73673266
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: AzScope object [Security],CreateRole method, CreateRole, CreateRole method [Security], CreateRole method [Security],AzScope object, CreateRole method [Security],IAzScope interface, IAzScope interface [Security],CreateRole method, IAzScope.CreateRole, IAzScope::CreateRole, azroles/IAzScope::CreateRole, security.iazscope_createrole
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
 - IAzScope.CreateRole
 - AzScope.CreateRole
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzScope::CreateRole


## -description


The <b>CreateRole</b> method creates an <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object with the specified name.


## -parameters




### -param bstrRoleName [in]

Name for the new <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppRole [out]

A pointer to a pointer to the created <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.




## -remarks



You must call the <a href="https://msdn.microsoft.com/97f2018a-92f0-4ebb-85f1-78c140003d8f">IAzRole::Submit</a> method to persist any changes made to the returned object.

The returned <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object is an immediate child object of the <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object.



