---
UID: NF:indexsrv.ISimpleCommandCreator.GetDefaultCatalog
title: ISimpleCommandCreator::GetDefaultCatalog (indexsrv.h)
author: windows-sdk-content
description: Determines the default catalog for the system.
old-location: search\isimplecommandcreator_getdefaultcatalog.htm
tech.root: search
ms.assetid: 6BD65290-209A-4FCA-BD2B-E4BB800C8BEF
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDefaultCatalog, GetDefaultCatalog method [search], GetDefaultCatalog method [search],ISimpleCommandCreator interface, ISimpleCommandCreator interface [search],GetDefaultCatalog method, ISimpleCommandCreator.GetDefaultCatalog, ISimpleCommandCreator::GetDefaultCatalog, indexsrv/ISimpleCommandCreator::GetDefaultCatalog, search.isimplecommandcreator_getdefaultcatalog
ms.topic: method
f1_keywords: 
 - "indexsrv/ISimpleCommandCreator.GetDefaultCatalog"
req.header: indexsrv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - COM
api_location:
 - Indexsrv.h
api_name:
 - ISimpleCommandCreator.GetDefaultCatalog
targetos: Windows
req.typenames: 
req.redist: Windows NT 4.0 Option Pack
ms.custom: 19H1
---

# ISimpleCommandCreator::GetDefaultCatalog


## -description


Determines the default catalog for the system.


## -parameters




### -param pwszCatalogName

The catalog name.


### -param cwcIn

The size in characters of <i>pwszCatalogName</i>.


### -param pcwcOut

Size of the catalog name.


## -returns



If this method succeeds, it returns the contents of the IsapiDefaultCatalogDirectory registry value. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nn-indexsrv-isimplecommandcreator">ISimpleCommandCreator</a>
 

 

