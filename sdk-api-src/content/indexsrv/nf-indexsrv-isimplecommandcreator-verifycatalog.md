---
UID: NF:indexsrv.ISimpleCommandCreator.VerifyCatalog
title: ISimpleCommandCreator::VerifyCatalog
author: windows-sdk-content
description: Validates the catalog location.
old-location: search\isimplecommandcreator_verifycatalog.htm
tech.root: search
ms.assetid: F4B1558D-F244-40ED-92C2-F5CC0B63AD50
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: ISimpleCommandCreator interface [search],VerifyCatalog method, ISimpleCommandCreator.VerifyCatalog, ISimpleCommandCreator::VerifyCatalog, VerifyCatalog, VerifyCatalog method [search], VerifyCatalog method [search],ISimpleCommandCreator interface, indexsrv/ISimpleCommandCreator::VerifyCatalog, search.isimplecommandcreator_verifycatalog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ISimpleCommandCreator.VerifyCatalog
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows NT 4.0 Option Pack
---

# ISimpleCommandCreator::VerifyCatalog


## -description


Validates the catalog location.


## -parameters




### -param pwszMachine

Machine on which the catalog exists.


### -param pwszCatalogName

The catalog name.


## -returns



If the catalog is accessible, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/CAC6BE83-863B-4DB0-B4FF-40029C242AE9">ISimpleCommandCreator</a>
 

 

