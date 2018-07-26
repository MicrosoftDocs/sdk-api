---
UID: NF:azroles.IAzClientContext2.AddRoles
title: IAzClientContext2::AddRoles
author: windows-sdk-content
description: Adds the specified array of existing IAzRole objects to the client context.
old-location: security\iazclientcontext2_addroles.htm
old-project: secauthz
ms.assetid: fa81e935-1207-44dd-85cb-215f754575fe
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: AddRoles, AddRoles method [Security], AddRoles method [Security],IAzClientContext2 interface, IAzClientContext2 interface [Security],AddRoles method, IAzClientContext2.AddRoles, IAzClientContext2::AddRoles, azroles/IAzClientContext2::AddRoles, security.iazclientcontext2_addroles
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
 - IAzClientContext2.AddRoles
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzClientContext2::AddRoles


## -description


The <b>AddRoles</b> method adds the specified array of existing <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> objects to the client context.


## -parameters




### -param varRoles [in]

The array of role names that specify the <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> objects to add to the client context.


### -param bstrScopeName [in]

The scope to which the array of roles applies.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> objects associated with the names in the <i>varRoles</i> array must already exist in the specified scope.

The added roles are used in subsequent calls to the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> and <a href="https://msdn.microsoft.com/753506cc-ed44-4795-90e5-c76010181d8a">GetRoles</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a>



<a href="https://msdn.microsoft.com/753506cc-ed44-4795-90e5-c76010181d8a">GetRoles</a>



<a href="https://msdn.microsoft.com/8e922370-18e3-481c-93f2-9a56d7898ba7">IAzClientContext2</a>
 

 

