---
UID: NF:azroles.IAzApplication.CreateApplicationGroup
title: IAzApplication::CreateApplicationGroup (azroles.h)
description: Creates an IAzApplicationGroup object with the specified name. (IAzApplication.CreateApplicationGroup)
helpviewer_keywords: ["AzApplication object [Security]","CreateApplicationGroup method","CreateApplicationGroup","CreateApplicationGroup method [Security]","CreateApplicationGroup method [Security]","AzApplication object","CreateApplicationGroup method [Security]","IAzApplication interface","IAzApplication interface [Security]","CreateApplicationGroup method","IAzApplication.CreateApplicationGroup","IAzApplication::CreateApplicationGroup","azroles/IAzApplication::CreateApplicationGroup","security.iazapplication_createapplicationgroup"]
old-location: security\iazapplication_createapplicationgroup.htm
tech.root: security
ms.assetid: 86f1694e-09a4-4a53-ae63-cfdb5d2e44ed
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],CreateApplicationGroup method, CreateApplicationGroup, CreateApplicationGroup method [Security], CreateApplicationGroup method [Security],AzApplication object, CreateApplicationGroup method [Security],IAzApplication interface, IAzApplication interface [Security],CreateApplicationGroup method, IAzApplication.CreateApplicationGroup, IAzApplication::CreateApplicationGroup, azroles/IAzApplication::CreateApplicationGroup, security.iazapplication_createapplicationgroup
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
 - IAzApplication::CreateApplicationGroup
 - azroles/IAzApplication::CreateApplicationGroup
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
 - IAzApplication.CreateApplicationGroup
 - AzApplication.CreateApplicationGroup
---

# IAzApplication::CreateApplicationGroup


## -description

The <b>CreateApplicationGroup</b> method creates an <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object with the specified name.

## -parameters

### -param bstrGroupName [in]

Name for the new <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object.

### -param varReserved [in, optional]

Reserved for future use.

### -param ppGroup [out]

A pointer to a pointer to the created <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object.

## -returns

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-submit">IAzApplicationGroup::Submit</a> method to persist any changes made to the returned object.

The returned <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object is an immediate child object of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.
