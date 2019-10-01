---
UID: NF:azroles.IAzScope.DeletePolicyReader
title: IAzScope::DeletePolicyReader (azroles.h)
author: windows-sdk-content
description: The DeletePolicyReader method of IAzScope removes the specified security identifier in text form from the list of principals that act as policy readers.
old-location: security\iazscope_deletepolicyreader.htm
tech.root: SecAuthZ
ms.assetid: c328a838-ae81-463d-8aa5-827071f58747
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AzScope object [Security],DeletePolicyReader method, DeletePolicyReader, DeletePolicyReader method [Security], DeletePolicyReader method [Security],AzScope object, DeletePolicyReader method [Security],IAzScope interface, IAzScope interface [Security],DeletePolicyReader method, IAzScope.DeletePolicyReader, IAzScope::DeletePolicyReader, azroles/IAzScope::DeletePolicyReader, security.iazscope_deletepolicyreader
ms.topic: method
f1_keywords: 
 - "azroles/IAzScope.DeletePolicyReader"
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
 - IAzScope.DeletePolicyReader
 - AzScope.DeletePolicyReader
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzScope::DeletePolicyReader


## -description


The <b>DeletePolicyReader</b> method removes the specified <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) in text form from the list of principals that act as policy readers.


## -parameters




### -param bstrReader [in]

Text form of the SID to remove from the list of policy readers.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">AccessCheck</a> method. Readers cannot modify the object or its child objects.

To view the list of policy readers, use the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazscope-get_policyreaders">PolicyReaders</a> property.



