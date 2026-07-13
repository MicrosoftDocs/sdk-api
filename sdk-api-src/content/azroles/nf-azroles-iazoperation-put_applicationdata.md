---
UID: NF:azroles.IAzOperation.put_ApplicationData
title: IAzOperation::put_ApplicationData (azroles.h)
description: The ApplicationData property of IAzOperation sets or retrieves an opaque field that can be used by the application to store information. (Put)
helpviewer_keywords: ["ApplicationData property [Security]","ApplicationData property [Security]","AzOperation object","ApplicationData property [Security]","IAzOperation interface","AzOperation object [Security]","ApplicationData property","IAzOperation interface [Security]","ApplicationData property","IAzOperation.ApplicationData","IAzOperation.put_ApplicationData","IAzOperation::ApplicationData","IAzOperation::get_ApplicationData","IAzOperation::put_ApplicationData","azroles/IAzOperation::ApplicationData","azroles/IAzOperation::get_ApplicationData","azroles/IAzOperation::put_ApplicationData","put_ApplicationData","security.iazoperation_applicationdata"]
old-location: security\iazoperation_applicationdata.htm
tech.root: security
ms.assetid: d4d22aae-6ca3-4a97-aa44-fa07674dc556
ms.date: 12/05/2018
ms.keywords: ApplicationData property [Security], ApplicationData property [Security],AzOperation object, ApplicationData property [Security],IAzOperation interface, AzOperation object [Security],ApplicationData property, IAzOperation interface [Security],ApplicationData property, IAzOperation.ApplicationData, IAzOperation.put_ApplicationData, IAzOperation::ApplicationData, IAzOperation::get_ApplicationData, IAzOperation::put_ApplicationData, azroles/IAzOperation::ApplicationData, azroles/IAzOperation::get_ApplicationData, azroles/IAzOperation::put_ApplicationData, put_ApplicationData, security.iazoperation_applicationdata
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
 - IAzOperation::put_ApplicationData
 - azroles/IAzOperation::put_ApplicationData
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
 - IAzOperation.ApplicationData
 - IAzOperation.get_ApplicationData
 - IAzOperation.put_ApplicationData
 - AzOperation.ApplicationData
---

# IAzOperation::put_ApplicationData


## -description

The <b>ApplicationData</b> property sets or retrieves an opaque field that can be used by the application to store information.

This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Important</b>  Policy administrators can read from and write to this property. Applications should not store data in the <b>ApplicationData</b> property that should not be available to the policy administrator.</div>
<div> </div>

