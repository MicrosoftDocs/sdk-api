---
UID: NF:azroles.IAzApplication.get_Scopes
title: IAzApplication::get_Scopes
author: windows-sdk-content
description: Retrieves an IAzScopes object that is used to enumerate IAzScope objects from the policy data.
old-location: security\iazapplication_scopes.htm
tech.root: SecAuthZ
ms.assetid: cb56e48c-5c36-49f5-927e-417bfb59f940
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: AzApplication object [Security],Scopes property, IAzApplication interface [Security],Scopes property, IAzApplication.Scopes, IAzApplication.get_Scopes, IAzApplication::Scopes, IAzApplication::get_Scopes, Scopes property [Security], Scopes property [Security],AzApplication object, Scopes property [Security],IAzApplication interface, azroles/IAzApplication::Scopes, azroles/IAzApplication::get_Scopes, get_Scopes, security.iazapplication_scopes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IAzApplication.Scopes
 - IAzApplication.get_Scopes
 - AzApplication.Scopes
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplication::get_Scopes


## -description


The <b>Scopes</b> property retrieves an <a href="https://msdn.microsoft.com/f00953bf-b90a-4812-a87d-a66b98a2e95f">IAzScopes</a> object that is used to enumerate <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> objects from the policy data.

This property is read-only.


## -parameters


## -remarks



This property can be used only to enumerate <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> objects that are direct child objects of the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object.



