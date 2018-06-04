---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _SecPkgContext_NativeNamesW structure


## -description


The <b>SecPkgContext_NativeNames</b> structure returns the client and server principal names from the outbound ticket. This structure is valid only for client outbound tickets. This structure is returned by  <a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a>.


## -struct-fields




### -field sClientName

Pointer to a null-terminated string that represents the principal name for the client in the outbound ticket. This string should never be <b>NULL</b> when querying a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> negotiated with <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Kerberos</a>.


### -field sServerName

Pointer to a null-terminated string that represents the principal name for the server in the outbound ticket. This string should never be <b>NULL</b> when querying a security context negotiated with Kerberos.

