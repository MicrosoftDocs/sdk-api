---
UID: NF:azroles.IAzScope.OpenApplicationGroup
title: IAzScope::OpenApplicationGroup (azroles.h)
description: Opens an IAzApplicationGroup object by specifying its name. (IAzScope.OpenApplicationGroup)
helpviewer_keywords: ["AzScope object [Security]","OpenApplicationGroup method","IAzScope interface [Security]","OpenApplicationGroup method","IAzScope.OpenApplicationGroup","IAzScope::OpenApplicationGroup","OpenApplicationGroup","OpenApplicationGroup method [Security]","OpenApplicationGroup method [Security]","AzScope object","OpenApplicationGroup method [Security]","IAzScope interface","azroles/IAzScope::OpenApplicationGroup","security.iazscope_openapplicationgroup"]
old-location: security\iazscope_openapplicationgroup.htm
tech.root: security
ms.assetid: 6c0e2832-e46b-428e-8f0b-ca1d816afaeb
ms.date: 12/05/2018
ms.keywords: AzScope object [Security],OpenApplicationGroup method, IAzScope interface [Security],OpenApplicationGroup method, IAzScope.OpenApplicationGroup, IAzScope::OpenApplicationGroup, OpenApplicationGroup, OpenApplicationGroup method [Security], OpenApplicationGroup method [Security],AzScope object, OpenApplicationGroup method [Security],IAzScope interface, azroles/IAzScope::OpenApplicationGroup, security.iazscope_openapplicationgroup
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
 - IAzScope::OpenApplicationGroup
 - azroles/IAzScope::OpenApplicationGroup
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
 - IAzScope.OpenApplicationGroup
 - AzScope.OpenApplicationGroup
---

# IAzScope::OpenApplicationGroup


## -description

The <b>OpenApplicationGroup</b> method opens an <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object with the specified name.

## -parameters

### -param bstrGroupName [in]

Name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object to open.

### -param varReserved [in, optional]

Reserved for future use.

### -param ppGroup [out]

A pointer to a pointer to the opened <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.
