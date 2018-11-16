---
UID: NS:winnt._TOKEN_APPCONTAINER_INFORMATION
title: "_TOKEN_APPCONTAINER_INFORMATION"
author: windows-sdk-content
description: Specifies all the information in a token that is necessary for an app container.
old-location: security\token_appcontainer_information.htm
tech.root: SecAuthZ
ms.assetid: 6038C7E9-AED6-49D2-8D96-907E973A64B1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PTOKEN_APPCONTAINER_INFORMATION, PTOKEN_APPCONTAINER_INFORMATION, PTOKEN_APPCONTAINER_INFORMATION structure pointer [Security], TOKEN_APPCONTAINER_INFORMATION, TOKEN_APPCONTAINER_INFORMATION structure [Security], _TOKEN_APPCONTAINER_INFORMATION, security.token_appcontainer_information, winnt/PTOKEN_APPCONTAINER_INFORMATION, winnt/TOKEN_APPCONTAINER_INFORMATION"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TOKEN_APPCONTAINER_INFORMATION
product: Windows
targetos: Windows
req.typenames: TOKEN_APPCONTAINER_INFORMATION, *PTOKEN_APPCONTAINER_INFORMATION
req.redist: 
---

# _TOKEN_APPCONTAINER_INFORMATION structure


## -description


The <b>TOKEN_APPCONTAINER_INFORMATION</b> structure specifies all the information in a token that is necessary for an app container.


## -struct-fields




### -field TokenAppContainer

The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) of the app container.

