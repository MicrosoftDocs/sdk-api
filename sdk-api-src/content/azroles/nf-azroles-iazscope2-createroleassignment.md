---
UID: NF:azroles.IAzScope2.CreateRoleAssignment
title: IAzScope2::CreateRoleAssignment
author: windows-sdk-content
description: Creates a new IAzRoleAssignment object with the specified name in this scope.
old-location: security\iazscope2_createroleassignment.htm
tech.root: secauthz
ms.assetid: 98cb412b-9742-4f94-a470-61e675f6b253
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CreateRoleAssignment, CreateRoleAssignment method [Security], CreateRoleAssignment method [Security],IAzScope2 interface, IAzScope2 interface [Security],CreateRoleAssignment method, IAzScope2.CreateRoleAssignment, IAzScope2::CreateRoleAssignment, azroles/IAzScope2::CreateRoleAssignment, security.iazscope2_createroleassignment
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
 - IAzScope2.CreateRoleAssignment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzScope2::CreateRoleAssignment


## -description


The <b>CreateRoleAssignment</b> method creates a new <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object with the specified name in this scope.


## -parameters




### -param bstrRoleAssignmentName [in]

A string that contains the name of the new <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object.


### -param ppRoleAssignment [out]

The address of  a pointer to the <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object that this method creates.

When you have finished using the <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object, release it by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



