---
UID: NF:azroles.IAzApplication.OpenApplicationGroup
title: IAzApplication::OpenApplicationGroup (azroles.h)
description: Opens an IAzApplicationGroup object by specifying its name. (IAzApplication.OpenApplicationGroup)
helpviewer_keywords: ["AzApplication object [Security]","OpenApplicationGroup method","IAzApplication interface [Security]","OpenApplicationGroup method","IAzApplication.OpenApplicationGroup","IAzApplication::OpenApplicationGroup","OpenApplicationGroup","OpenApplicationGroup method [Security]","OpenApplicationGroup method [Security]","AzApplication object","OpenApplicationGroup method [Security]","IAzApplication interface","azroles/IAzApplication::OpenApplicationGroup","security.iazapplication_openapplicationgroup"]
old-location: security\iazapplication_openapplicationgroup.htm
tech.root: security
ms.assetid: 6f9c9d65-73aa-40e9-bd04-d4d5d4370201
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],OpenApplicationGroup method, IAzApplication interface [Security],OpenApplicationGroup method, IAzApplication.OpenApplicationGroup, IAzApplication::OpenApplicationGroup, OpenApplicationGroup, OpenApplicationGroup method [Security], OpenApplicationGroup method [Security],AzApplication object, OpenApplicationGroup method [Security],IAzApplication interface, azroles/IAzApplication::OpenApplicationGroup, security.iazapplication_openapplicationgroup
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
 - IAzApplication::OpenApplicationGroup
 - azroles/IAzApplication::OpenApplicationGroup
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
 - IAzApplication.OpenApplicationGroup
 - AzApplication.OpenApplicationGroup
---

# IAzApplication::OpenApplicationGroup


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

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.
