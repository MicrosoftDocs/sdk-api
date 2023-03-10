---
UID: NF:azroles.IAzAuthorizationStore.AddPolicyReader
title: IAzAuthorizationStore::AddPolicyReader (azroles.h)
description: Adds the specified security identifier (SID) in text form to the list of principals that act as policy readers. (IAzAuthorizationStore.AddPolicyReader)
helpviewer_keywords: ["AddPolicyReader","AddPolicyReader method [Security]","AddPolicyReader method [Security]","AzAuthorizationStore object","AddPolicyReader method [Security]","IAzAuthorizationStore interface","AzAuthorizationStore object [Security]","AddPolicyReader method","IAzAuthorizationStore interface [Security]","AddPolicyReader method","IAzAuthorizationStore.AddPolicyReader","IAzAuthorizationStore::AddPolicyReader","azroles/IAzAuthorizationStore::AddPolicyReader","security.azauthorizationstore_addpolicyreader"]
old-location: security\azauthorizationstore_addpolicyreader.htm
tech.root: security
ms.assetid: 52872839-1066-4a43-8549-b7f37a0ebe40
ms.date: 12/05/2018
ms.keywords: AddPolicyReader, AddPolicyReader method [Security], AddPolicyReader method [Security],AzAuthorizationStore object, AddPolicyReader method [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],AddPolicyReader method, IAzAuthorizationStore interface [Security],AddPolicyReader method, IAzAuthorizationStore.AddPolicyReader, IAzAuthorizationStore::AddPolicyReader, azroles/IAzAuthorizationStore::AddPolicyReader, security.azauthorizationstore_addpolicyreader
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
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzAuthorizationStore::AddPolicyReader
 - azroles/IAzAuthorizationStore::AddPolicyReader
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
 - AzAuthorizationStore.AddPolicyReader
 - IAzAuthorizationStore.AddPolicyReader
---

# IAzAuthorizationStore::AddPolicyReader


## -description

The <b>AddPolicyReader</b> method adds the specified <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) in text form to the list of principals that act as policy readers.

## -parameters

### -param bstrReader [in]

Text form of the  SID to add to the list of policy readers.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the  <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">AccessCheck</a> method. Readers cannot modify the object or its child objects.

To view the list of policy readers, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_policyreaders">PolicyReaders</a> property.

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-submit">Submit</a> method to persist any changes made by this method.
