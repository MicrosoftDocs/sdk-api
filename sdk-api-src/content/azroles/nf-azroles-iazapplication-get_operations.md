---
UID: NF:azroles.IAzApplication.get_Operations
title: IAzApplication::get_Operations (azroles.h)
description: Retrieves an IAzOperations object that is used to enumerate IAzOperation objects from the policy data.
helpviewer_keywords: ["AzApplication object [Security]","Operations property","IAzApplication interface [Security]","Operations property","IAzApplication.Operations","IAzApplication.get_Operations","IAzApplication::Operations","IAzApplication::get_Operations","Operations property [Security]","Operations property [Security]","AzApplication object","Operations property [Security]","IAzApplication interface","azroles/IAzApplication::Operations","azroles/IAzApplication::get_Operations","get_Operations","security.iazapplication_operations"]
old-location: security\iazapplication_operations.htm
tech.root: security
ms.assetid: 274a130a-3a3c-46fc-9d2a-3123cdc98d4b
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],Operations property, IAzApplication interface [Security],Operations property, IAzApplication.Operations, IAzApplication.get_Operations, IAzApplication::Operations, IAzApplication::get_Operations, Operations property [Security], Operations property [Security],AzApplication object, Operations property [Security],IAzApplication interface, azroles/IAzApplication::Operations, azroles/IAzApplication::get_Operations, get_Operations, security.iazapplication_operations
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
 - IAzApplication::get_Operations
 - azroles/IAzApplication::get_Operations
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
 - IAzApplication.Operations
 - IAzApplication.get_Operations
 - AzApplication.Operations
---

# IAzApplication::get_Operations


## -description

The <b>Operations</b> property retrieves an <a href="/windows/desktop/api/azroles/nn-azroles-iazoperations">IAzOperations</a> object that is used to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> objects from the policy data.

This property is read-only.

## -parameters

## -remarks

This property can be used only to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> objects that are direct child objects of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.