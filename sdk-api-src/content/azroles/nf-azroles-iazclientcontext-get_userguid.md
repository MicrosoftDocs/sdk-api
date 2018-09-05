---
UID: NF:azroles.IAzClientContext.get_UserGuid
title: IAzClientContext::get_UserGuid
author: windows-sdk-content
description: Retrieves the name of the current client in GUID format.
old-location: security\iazclientcontext_userguid.htm
old-project: SecAuthZ
ms.assetid: fd60d1d0-67b9-457f-a01e-6ea470d9db6a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AzClientContext object [Security],UserGuid property, IAzClientContext interface [Security],UserGuid property, IAzClientContext.UserGuid, IAzClientContext.get_UserGuid, IAzClientContext::UserGuid, IAzClientContext::get_UserGuid, UserGuid property [Security], UserGuid property [Security],AzClientContext object, UserGuid property [Security],IAzClientContext interface, azroles/IAzClientContext::UserGuid, azroles/IAzClientContext::get_UserGuid, get_UserGuid, security.iazclientcontext_userguid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzClientContext.UserGuid
 - IAzClientContext.get_UserGuid
 - AzClientContext.UserGuid
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzClientContext::get_UserGuid


## -description


The <b>UserGuid</b> property retrieves the name of the current client in GUID format.

This property is read-only.


## -parameters


## -remarks



The GUID client name is retrieved by impersonating the client token and calling the <a href="https://msdn.microsoft.com/7e7d618b-2e64-4b0b-aed3-f3221b0443ca">GetUserNameEx</a> function with <b>NameUniqueId</b> specified for the <i>NameFormat</i> parameter. 

An example of a  client name in GUID format is "{4fa050f0-f561-11cf-bdd9-00aa003a77b6}Ben Smith".



