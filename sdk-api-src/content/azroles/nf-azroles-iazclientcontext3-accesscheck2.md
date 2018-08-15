---
UID: NF:azroles.IAzClientContext3.AccessCheck2
title: IAzClientContext3::AccessCheck2
author: windows-sdk-content
description: Returns a value that specifies whether the principal represented by the current client context is allowed to perform the specified operation.
old-location: security\iazclientcontext3_accesscheck2_method.htm
old-project: secauthz
ms.assetid: 042d1f51-5eb8-4c32-97f1-bb76546e6624
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AccessCheck2, AccessCheck2 method [Security], AccessCheck2 method [Security],IAzClientContext3 interface, IAzClientContext3 interface [Security],AccessCheck2 method, IAzClientContext3.AccessCheck2, IAzClientContext3::AccessCheck2, azroles/IAzClientContext3::AccessCheck2, security.iazclientcontext3_accesscheck2_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Azroles.idl
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
 - Azroles.h
api_name:
 - IAzClientContext3.AccessCheck2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAzClientContext3::AccessCheck2


## -description


The <b>AccessCheck2</b> method returns a value that specifies whether the principal represented by the current client context is allowed to perform the specified operation.


## -parameters




### -param bstrObjectName [in]

The name of the accessed object. This string is used in audits.


### -param bstrScopeName [in]

The name of the scope that contains the operation specified by the <i>lOperation</i> parameter.


### -param lOperation [in]

The <a href="https://msdn.microsoft.com/3466dea1-b005-40fc-87d1-29b5e033f6a0">OperationID</a> property of the <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object for which to check access.


### -param plResult [out]

A pointer to a value that indicates whether the principal represented by the current client context is allowed to perform the operation specified by the <i>lOperation</i> parameter.

 A value of <b>NO_ERROR</b> indicates that the principal does have permission. Any other value indicates that the principal does not have permission.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



