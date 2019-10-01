---
UID: NF:azroles.IAzScope2.OpenRoleAssignment
title: IAzScope2::OpenRoleAssignment (azroles.h)
author: windows-sdk-content
description: Opens an IAzRoleAssignment object with the specified name in this scope.
old-location: security\iazscope2_openroleassignment.htm
tech.root: SecAuthZ
ms.assetid: cb7560d0-da5c-444d-9944-b6db980985bc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAzScope2 interface [Security],OpenRoleAssignment method, IAzScope2.OpenRoleAssignment, IAzScope2::OpenRoleAssignment, OpenRoleAssignment, OpenRoleAssignment method [Security], OpenRoleAssignment method [Security],IAzScope2 interface, azroles/IAzScope2::OpenRoleAssignment, security.iazscope2_openroleassignment
ms.topic: method
f1_keywords: 
 - "azroles/IAzScope2.OpenRoleAssignment"
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
 - IAzScope2.OpenRoleAssignment
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAzScope2::OpenRoleAssignment


## -description


The <b>OpenRoleAssignment</b> method opens an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object with the specified name in this scope.


## -parameters




### -param bstrRoleAssignmentName [in]

A string that contains the name of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object to open.


### -param ppRoleAssignment [out]

The address of a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object that this method opens.

When you have finished using the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object, release it by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.



