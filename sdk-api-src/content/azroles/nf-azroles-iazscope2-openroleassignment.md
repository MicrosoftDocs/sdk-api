---
UID: NF:azroles.IAzScope2.OpenRoleAssignment
title: IAzScope2::OpenRoleAssignment
author: windows-driver-content
description: Opens an IAzRoleAssignment object with the specified name in this scope.
old-location: security\iazscope2_openroleassignment.htm
old-project: SecAuthZ
ms.assetid: cb7560d0-da5c-444d-9944-b6db980985bc
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IAzScope2 interface [Security],OpenRoleAssignment method, IAzScope2.OpenRoleAssignment, IAzScope2::OpenRoleAssignment, OpenRoleAssignment, OpenRoleAssignment method [Security], OpenRoleAssignment method [Security],IAzScope2 interface, azroles/IAzScope2::OpenRoleAssignment, security.iazscope2_openroleassignment
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzScope2.OpenRoleAssignment
product: Windows
targetos: Windows
req.lib: 
req.dll: Azroles.dll
req.irql: 
---

# IAzScope2::OpenRoleAssignment


## -description


The <b>OpenRoleAssignment</b> method opens an <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object with the specified name in this scope.


## -parameters




### -param bstrRoleAssignmentName [in]

A string that contains the name of the <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object to open.


### -param ppRoleAssignment [out]

The address of a pointer to the <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object that this method opens.

When you have finished using the <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object, release it by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



