---
UID: NF:azroles.IAzClientContext3.AccessCheck2
title: IAzClientContext3::AccessCheck2 (azroles.h)
author: windows-sdk-content
description: Returns a value that specifies whether the principal represented by the current client context is allowed to perform the specified operation.
old-location: security\iazclientcontext3_accesscheck2_method.htm
tech.root: SecAuthZ
ms.assetid: 042d1f51-5eb8-4c32-97f1-bb76546e6624
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AccessCheck2, AccessCheck2 method [Security], AccessCheck2 method [Security],IAzClientContext3 interface, IAzClientContext3 interface [Security],AccessCheck2 method, IAzClientContext3.AccessCheck2, IAzClientContext3::AccessCheck2, azroles/IAzClientContext3::AccessCheck2, security.iazclientcontext3_accesscheck2_method
ms.topic: method
f1_keywords: 
 - "azroles/IAzClientContext3.AccessCheck2"
dev_langs:
 - c++
req.header: azroles.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzClientContext3.AccessCheck2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

The <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazoperation-get_operationid">OperationID</a> property of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object for which to check access.


### -param plResult [out]

A pointer to a value that indicates whether the principal represented by the current client context is allowed to perform the operation specified by the <i>lOperation</i> parameter.

 A value of <b>NO_ERROR</b> indicates that the principal does have permission. Any other value indicates that the principal does not have permission.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.



