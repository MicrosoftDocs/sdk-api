---
UID: NF:azroles.IAzScope.CreateApplicationGroup
title: IAzScope::CreateApplicationGroup
author: windows-sdk-content
description: Creates an IAzApplicationGroup object with the specified name.
old-location: security\iazscope_createapplicationgroup.htm
tech.root: SecAuthZ
ms.assetid: 9bceb3a9-1144-48a1-a4d4-e612a3e77942
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: AzScope object [Security],CreateApplicationGroup method, CreateApplicationGroup, CreateApplicationGroup method [Security], CreateApplicationGroup method [Security],AzScope object, CreateApplicationGroup method [Security],IAzScope interface, IAzScope interface [Security],CreateApplicationGroup method, IAzScope.CreateApplicationGroup, IAzScope::CreateApplicationGroup, azroles/IAzScope::CreateApplicationGroup, security.iazscope_createapplicationgroup
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
 - IAzScope.CreateApplicationGroup
 - AzScope.CreateApplicationGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzScope::CreateApplicationGroup


## -description


The <b>CreateApplicationGroup</b> method creates an <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object with the specified name.


## -parameters




### -param bstrGroupName [in]

Name for the new <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppGroup [out]

A pointer to a pointer to the created <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.




## -remarks



You must call the <a href="https://msdn.microsoft.com/en-us/library/Aa377322(v=VS.85).aspx">IAzApplicationGroup::Submit</a> method to persist any changes made to the returned object.

The returned <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object is an immediate child object of the <a href="https://msdn.microsoft.com/en-us/library/Aa378237(v=VS.85).aspx">IAzScope</a> object.



