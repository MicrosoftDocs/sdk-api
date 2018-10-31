---
UID: NF:azroles.IAzClientContext2.AddApplicationGroups
title: IAzClientContext2::AddApplicationGroups
author: windows-sdk-content
description: Adds the specified array of existing IAzApplicationGroup objects to the client context object.
old-location: security\iazclientcontext2_addapplicationgroups.htm
tech.root: secauthz
ms.assetid: 8ad7c7df-0bdd-4ea1-9a9e-98323b82c0b0
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AddApplicationGroups, AddApplicationGroups method [Security], AddApplicationGroups method [Security],IAzClientContext2 interface, IAzClientContext2 interface [Security],AddApplicationGroups method, IAzClientContext2.AddApplicationGroups, IAzClientContext2::AddApplicationGroups, azroles/IAzClientContext2::AddApplicationGroups, security.iazclientcontext2_addapplicationgroups
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAzClientContext2.AddApplicationGroups
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzClientContext2::AddApplicationGroups


## -description


The <b>AddApplicationGroups</b> method adds the specified array of existing <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> objects to the client context object.


## -parameters




### -param varApplicationGroups [in]

The array of <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> objects to add.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> objects in the <i>varApplicationGroups</i> array must already exist in the authorization store.

The added roles are used in subsequent calls to the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> and <a href="https://msdn.microsoft.com/753506cc-ed44-4795-90e5-c76010181d8a">GetRoles</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a>



<a href="https://msdn.microsoft.com/753506cc-ed44-4795-90e5-c76010181d8a">GetRoles</a>



<a href="https://msdn.microsoft.com/8e922370-18e3-481c-93f2-9a56d7898ba7">IAzClientContext2</a>
 

 

