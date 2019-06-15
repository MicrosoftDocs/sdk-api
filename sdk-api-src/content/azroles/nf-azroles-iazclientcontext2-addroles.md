---
UID: NF:azroles.IAzClientContext2.AddRoles
title: IAzClientContext2::AddRoles (azroles.h)
author: windows-sdk-content
description: Adds the specified array of existing IAzRole objects to the client context.
old-location: security\iazclientcontext2_addroles.htm
tech.root: SecAuthZ
ms.assetid: fa81e935-1207-44dd-85cb-215f754575fe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddRoles, AddRoles method [Security], AddRoles method [Security],IAzClientContext2 interface, IAzClientContext2 interface [Security],AddRoles method, IAzClientContext2.AddRoles, IAzClientContext2::AddRoles, azroles/IAzClientContext2::AddRoles, security.iazclientcontext2_addroles
ms.topic: method
f1_keywords: ["azroles/IAzClientContext2.AddRoles"]
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
 - IAzClientContext2.AddRoles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAzClientContext2::AddRoles


## -description


The <b>AddRoles</b> method adds the specified array of existing <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> objects to the client context.


## -parameters




### -param varRoles [in]

The array of role names that specify the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> objects to add to the client context.


### -param bstrScopeName [in]

The scope to which the array of roles applies.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> objects associated with the names in the <i>varRoles</i> array must already exist in the specified scope.

The added roles are used in subsequent calls to the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">AccessCheck</a> and <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext-getroles">GetRoles</a> methods.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">AccessCheck</a>



<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext-getroles">GetRoles</a>



<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazclientcontext2">IAzClientContext2</a>
 

 

