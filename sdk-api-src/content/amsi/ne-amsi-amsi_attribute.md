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

# AMSI_ATTRIBUTE enumeration


## -description


The <b>AMSI_ATTRIBUTE</b> enumeration specifies the types of attributes that can be requested by <a href="https://msdn.microsoft.com/7AD74D85-1A1E-4AFD-91C1-670AC7280285">IAmsiStream::GetAttribute</a>.


## -enum-fields




### -field AMSI_ATTRIBUTE_APP_NAME

Return the name, version, or GUID string of the calling application, copied from a <b>LPWSTR</b>.


### -field AMSI_ATTRIBUTE_CONTENT_NAME

Return the filename, URL, unique script ID, or similar of the content, copied from a <b>LPWSTR</b>.


### -field AMSI_ATTRIBUTE_CONTENT_SIZE

Return the  size of the input, as a <b>ULONGLONG</b>.


### -field AMSI_ATTRIBUTE_CONTENT_ADDRESS

Return the  memory address if the content is fully loaded into memory.


### -field AMSI_ATTRIBUTE_SESSION

Session is used to associate different scan calls, such as if the contents
    to be scanned belong to the sample original script. Return a <b>PVOID</b> to the next portion of the content to be scanned. Return <b>nullptr</b> if the content
    is self-contained.


### -field AMSI_ATTRIBUTE_REDIRECT_CHAIN_SIZE


### -field AMSI_ATTRIBUTE_REDIRECT_CHAIN_ADDRESS


### -field AMSI_ATTRIBUTE_ALL_SIZE


### -field AMSI_ATTRIBUTE_ALL_ADDRESS


### -field AMSI_ATTRIBUTE_QUIET



