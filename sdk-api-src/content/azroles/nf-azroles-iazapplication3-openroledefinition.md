---
UID: NF:azroles.IAzApplication3.OpenRoleDefinition
title: IAzApplication3::OpenRoleDefinition
author: windows-sdk-content
description: Opens an IAzRoleDefinition object with the specified name.
old-location: security\iazapplication3_openroledefinition.htm
tech.root: SecAuthZ
ms.assetid: 460b917c-a07b-4f50-b80f-0f6d986b65ff
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAzApplication3 interface [Security],OpenRoleDefinition method, IAzApplication3.OpenRoleDefinition, IAzApplication3::OpenRoleDefinition, OpenRoleDefinition, OpenRoleDefinition method [Security], OpenRoleDefinition method [Security],IAzApplication3 interface, azroles/IAzApplication3::OpenRoleDefinition, security.iazapplication3_openroledefinition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
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
 - IAzApplication3.OpenRoleDefinition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- azroles.h
: 
- IAzApplication3.OpenRoleDefinition
: 
---

# IAzApplication3::OpenRoleDefinition


## -description


The <b>OpenRoleDefinition</b> method opens an <a href="https://msdn.microsoft.com/en-us/library/Aa377927(v=VS.85).aspx">IAzRoleDefinition</a> object with the specified name.


## -parameters




### -param bstrRoleDefinitionName [in]

A string that contains the name of the <a href="https://msdn.microsoft.com/en-us/library/Aa377927(v=VS.85).aspx">IAzRoleDefinition</a> object to open.


### -param ppRoleDefinitions [out]

The address of a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Aa377927(v=VS.85).aspx">IAzRoleDefinition</a> object that this method opens.

When you have finished using this <a href="https://msdn.microsoft.com/en-us/library/Aa377927(v=VS.85).aspx">IAzRoleDefinition</a> object, release it by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method.


## -returns



 If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.



