---
UID: NF:structuredquery.ISchemaProvider.Localize
title: ISchemaProvider::Localize
author: windows-sdk-content
description: Localizes the currently loaded schema for a specified locale.
old-location: search\_search_ISchemaProvider_Localize.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ischemaprovider\localize.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISchemaProvider interface [search],Localize method, ISchemaProvider.Localize, ISchemaProvider::Localize, Localize, Localize method [search], Localize method [search],ISchemaProvider interface, _search_ISchemaProvider_Localize, search._search_ISchemaProvider_Localize, structuredquery/ISchemaProvider::Localize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquery.idl
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
 - Structuredquery.h
api_name:
 - ISchemaProvider.Localize
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
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



