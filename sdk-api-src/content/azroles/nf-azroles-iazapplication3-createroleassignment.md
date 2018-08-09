---
UID: NF:azroles.IAzApplication3.CreateRoleAssignment
title: IAzApplication3::CreateRoleAssignment
author: windows-sdk-content
description: Creates a new IAzRoleAssignment object with the specified name.
old-location: security\iazapplication3_createroleassignment.htm
old-project: secauthz
ms.assetid: 0646601d-97e6-437a-abfe-99fdb5bb1354
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateRoleAssignment, CreateRoleAssignment method [Security], CreateRoleAssignment method [Security],IAzApplication3 interface, IAzApplication3 interface [Security],CreateRoleAssignment method, IAzApplication3.CreateRoleAssignment, IAzApplication3::CreateRoleAssignment, azroles/IAzApplication3::CreateRoleAssignment, security.iazapplication3_createroleassignment
ms.prod: windows
ms.technology: windows-sdk
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
 - IAzApplication3.CreateRoleAssignment
product: Windows
targetos: Windows
req.lib: 
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication3::CreateRoleAssignment


## -description


The <b>CreateRoleAssignment</b> method creates a new <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object with the specified name.


## -parameters




### -param bstrRoleAssignmentName [in]

A string that contains the name of the new <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object.


### -param ppRoleAssignment [out]

The address of a pointer to the <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object that this method creates.

When you have finished using this <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object, release it by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



