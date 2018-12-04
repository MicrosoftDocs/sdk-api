---
UID: NF:azroles.IAzAuthorizationStore3.GetSchemaVersion
title: IAzAuthorizationStore3::GetSchemaVersion
author: windows-sdk-content
description: Gets the version number of this authorization store.
old-location: security\iazauthorizationstore3_getschemaversion_method.htm
tech.root: secauthz
ms.assetid: 263d8f04-8ed9-4801-86cf-51ede83436c7
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetSchemaVersion, GetSchemaVersion method [Security], GetSchemaVersion method [Security],IAzAuthorizationStore3 interface, IAzAuthorizationStore3 interface [Security],GetSchemaVersion method, IAzAuthorizationStore3.GetSchemaVersion, IAzAuthorizationStore3::GetSchemaVersion, azroles/IAzAuthorizationStore3::GetSchemaVersion, security.iazauthorizationstore3_getschemaversion_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Azroles.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzAuthorizationStore3.GetSchemaVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzAuthorizationStore3::GetSchemaVersion


## -description


The <b>GetSchemaVersion</b> method gets the version number of this authorization store.


## -parameters




### -param plMajorVersion [out]

The major version of the authorization store. Valid values are 1 and 2. A version 1 Authorization Manager (AzMan) runtime cannot read from or write to an authorization store with a major version of 2.


### -param plMinorVersion [out]

The minor version of the authorization store. Valid values are 1 and 2. A version 1 AzMan runtime can read from but not write to an authorization store with a minor version of 2.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



