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

# tagPARSEDURLW structure


## -description


Used by the <a href="https://msdn.microsoft.com/3d42dad0-b9eb-4e40-afc8-68cb85b27504">ParseURL</a> function to return the parsed URL.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

[in] The size of the structure, in bytes. The calling application must set this member before calling the <a href="https://msdn.microsoft.com/3d42dad0-b9eb-4e40-afc8-68cb85b27504">ParseURL</a> function.


### -field pszProtocol

Type: <b>LPCTSTR</b>

[out] A pointer to the beginning of the protocol part of the URL.


### -field cchProtocol

Type: <b>UINT</b>

The number of characters in the URL's protocol section.


### -field pszSuffix

Type: <b>LPCTSTR</b>

[out] A pointer to the section of the URL that follows the protocol and colon (':'). For file URLs, the function also skips the leading "//" characters.


### -field cchSuffix

Type: <b>UINT</b>

[out] The number of characters in the URL's suffix.


### -field nScheme

Type: <b>UINT</b>

[out] A value from the <a href="https://msdn.microsoft.com/45686920-356d-4dd7-8482-2427854a92ed">URL_SCHEME</a> enumeration that specifies the URL's scheme.

