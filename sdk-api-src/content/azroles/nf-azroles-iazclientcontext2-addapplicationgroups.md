---
UID: NF:azroles.IAzClientContext2.AddApplicationGroups
title: IAzClientContext2::AddApplicationGroups (azroles.h)
description: Adds the specified array of existing IAzApplicationGroup objects to the client context object.
helpviewer_keywords: ["AddApplicationGroups","AddApplicationGroups method [Security]","AddApplicationGroups method [Security]","IAzClientContext2 interface","IAzClientContext2 interface [Security]","AddApplicationGroups method","IAzClientContext2.AddApplicationGroups","IAzClientContext2::AddApplicationGroups","azroles/IAzClientContext2::AddApplicationGroups","security.iazclientcontext2_addapplicationgroups"]
old-location: security\iazclientcontext2_addapplicationgroups.htm
tech.root: security
ms.assetid: 8ad7c7df-0bdd-4ea1-9a9e-98323b82c0b0
ms.date: 12/05/2018
ms.keywords: AddApplicationGroups, AddApplicationGroups method [Security], AddApplicationGroups method [Security],IAzClientContext2 interface, IAzClientContext2 interface [Security],AddApplicationGroups method, IAzClientContext2.AddApplicationGroups, IAzClientContext2::AddApplicationGroups, azroles/IAzClientContext2::AddApplicationGroups, security.iazclientcontext2_addapplicationgroups
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAzClientContext2::AddApplicationGroups
 - azroles/IAzClientContext2::AddApplicationGroups
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzClientContext2.AddApplicationGroups
---

# IAzClientContext2::AddApplicationGroups


## -description

The <b>AddApplicationGroups</b> method adds the specified array of existing <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> objects to the client context object.

## -parameters

### -param varApplicationGroups [in]

The array of <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> objects to add.

## -returns

 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> objects in the <i>varApplicationGroups</i> array must already exist in the authorization store.

The added roles are used in subsequent calls to the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">AccessCheck</a> and <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-getroles">GetRoles</a> methods.

## -see-also

<a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">AccessCheck</a>



<a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-getroles">GetRoles</a>



<a href="/windows/desktop/api/azroles/nn-azroles-iazclientcontext2">IAzClientContext2</a>