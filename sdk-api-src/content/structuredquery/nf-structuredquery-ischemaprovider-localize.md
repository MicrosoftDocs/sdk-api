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

# ISchemaProvider::Localize


## -description


Localizes the currently loaded schema for a specified locale.


## -parameters




### -param lcid [in]

Type: <b>LCID</b>

The locale to localize for.


### -param pSchemaLocalizerSupport [in]

Type: <b><a href="https://msdn.microsoft.com/7db4c6ec-ba3a-49dd-bba5-3847d4d74e06">ISchemaLocalizerSupport</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/7db4c6ec-ba3a-49dd-bba5-3847d4d74e06">ISchemaLocalizerSupport</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before this method is called, the loaded schema should typically be a schema that is not localized, such as the one in %SYSTEMROOT%\System32\StructuredQuerySchema.bin. This method makes the loaded schema suitable for parsing queries in the specified locale, using the object specified in the <i>pSchemaLocalizerSupport</i> parameter. The localized schema can then be saved into a schema binary by calling the <a href="https://msdn.microsoft.com/f65a8cf8-91f4-400e-9deb-303f103de48b">ISchemaProvider::SaveBinary</a> method.

Most applications should use <a href="https://msdn.microsoft.com/22ae21a0-927e-4e76-856e-7285e4abfea3">CreateLoadedParser</a> to obtain a query parser loaded with a localized schema, instead of using this method explicitly.



