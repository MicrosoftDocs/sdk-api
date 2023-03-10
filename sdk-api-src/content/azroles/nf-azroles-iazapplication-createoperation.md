---
UID: NF:azroles.IAzApplication.CreateOperation
title: IAzApplication::CreateOperation (azroles.h)
description: Creates an IAzOperation object with the specified name.
helpviewer_keywords: ["AzApplication object [Security]","CreateOperation method","CreateOperation","CreateOperation method [Security]","CreateOperation method [Security]","AzApplication object","CreateOperation method [Security]","IAzApplication interface","IAzApplication interface [Security]","CreateOperation method","IAzApplication.CreateOperation","IAzApplication::CreateOperation","azroles/IAzApplication::CreateOperation","security.iazapplication_createoperation"]
old-location: security\iazapplication_createoperation.htm
tech.root: security
ms.assetid: 4faf4fc3-5847-40a1-9f85-fb10bb3048b4
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],CreateOperation method, CreateOperation, CreateOperation method [Security], CreateOperation method [Security],AzApplication object, CreateOperation method [Security],IAzApplication interface, IAzApplication interface [Security],CreateOperation method, IAzApplication.CreateOperation, IAzApplication::CreateOperation, azroles/IAzApplication::CreateOperation, security.iazapplication_createoperation
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
 - IAzApplication::CreateOperation
 - azroles/IAzApplication::CreateOperation
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
 - IAzApplication.CreateOperation
 - AzApplication.CreateOperation
---

# IAzApplication::CreateOperation


## -description

The <b>CreateOperation</b> method creates an <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object with the specified name.

## -parameters

### -param bstrOperationName [in]

Name for the new <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object.

### -param varReserved [in, optional]

Reserved for future use.

### -param ppOperation [out]

A pointer to a pointer to the created <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object.

## -returns

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazoperation-submit">IAzOperation::Submit</a> method to persist any changes made to the returned object.

The returned <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object is an immediate child object of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.