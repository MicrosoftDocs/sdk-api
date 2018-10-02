---
UID: NF:azroles.IAzApplication3.OpenRoleAssignment
title: IAzApplication3::OpenRoleAssignment
author: windows-sdk-content
description: Opens an IAzRoleAssignment object with the specified name.
old-location: security\iazapplication3_openroleassignment.htm
tech.root: SecAuthZ
ms.assetid: 2d0ec47e-5d5f-43d7-aace-fffca0037ac3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAzApplication3 interface [Security],OpenRoleAssignment method, IAzApplication3.OpenRoleAssignment, IAzApplication3::OpenRoleAssignment, OpenRoleAssignment, OpenRoleAssignment method [Security], OpenRoleAssignment method [Security],IAzApplication3 interface, azroles/IAzApplication3::OpenRoleAssignment, security.iazapplication3_openroleassignment
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
 - IAzApplication3.OpenRoleAssignment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzApplication3::OpenRoleAssignment


## -description


The <b>OpenRoleAssignment</b> method opens an <a href="https://msdn.microsoft.com/en-us/library/Aa377918(v=VS.85).aspx">IAzRoleAssignment</a> object with the specified name.


## -parameters




### -param bstrRoleAssignmentName [in]

A string that contains the name of the <a href="https://msdn.microsoft.com/en-us/library/Aa377918(v=VS.85).aspx">IAzRoleAssignment</a> object to open.


### -param ppRoleAssignment [out]

The address of a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Aa377918(v=VS.85).aspx">IAzRoleAssignment</a> object that this method opens.

When you have finished using this <a href="https://msdn.microsoft.com/en-us/library/Aa377918(v=VS.85).aspx">IAzRoleAssignment</a> object, release it by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.



