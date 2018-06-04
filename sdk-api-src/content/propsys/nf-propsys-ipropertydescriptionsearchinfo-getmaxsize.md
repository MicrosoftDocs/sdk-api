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

# IPropertyDescriptionSearchInfo::GetMaxSize


## -description


Gets the maximum size value from the property schema's <a href="shell.propdesc_schema_searchInfo">searchInfo</a> element.


## -parameters




### -param pcbMaxSize [out]

Type: <b>UINT*</b>

Pointer to a value that, when this method returns successfully, receives the value of the maxSize attribute of the <a href="shell.propdesc_schema_searchInfo">searchInfo</a> element. The default is:

                    

<ul>
<li><b>Windows Vista</b>: 128 bytes</li>
<li><b>Windows 7 and later</b>: 512 bytes</li>
</ul>

## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



