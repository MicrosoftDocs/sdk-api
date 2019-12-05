---
UID: NF:sbtsv.ITsSbProvider.CreateEnvironmentPropertySetObject
title: ITsSbProvider::CreateEnvironmentPropertySetObject (sbtsv.h)
description: Creates an ITsSbEnvironmentPropertySet environment property set object.
old-location: termserv\itssbprovider_createenvironmentpropertysetobject.htm
tech.root: TermServ
ms.assetid: 52bb5c05-f8eb-42c9-862f-d42e71507a91
ms.date: 12/05/2018
ms.keywords: CreateEnvironmentPropertySetObject, CreateEnvironmentPropertySetObject method [Remote Desktop Services], CreateEnvironmentPropertySetObject method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],CreateEnvironmentPropertySetObject method, ITsSbProvider.CreateEnvironmentPropertySetObject, ITsSbProvider::CreateEnvironmentPropertySetObject, sbtsv/ITsSbProvider::CreateEnvironmentPropertySetObject, termserv.itssbprovider_createenvironmentpropertysetobject
ms.topic: method
f1_keywords:
- sbtsv/ITsSbProvider.CreateEnvironmentPropertySetObject
dev_langs:
- c++
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
- sbtsv.h
api_name:
- ITsSbProvider.CreateEnvironmentPropertySetObject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbProvider::CreateEnvironmentPropertySetObject


## -description


Creates an <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset">ITsSbEnvironmentPropertySet</a> environment property set object.


## -parameters




### -param ppPropertySet [out]

A pointer to the created <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset">ITsSbEnvironmentPropertySet</a> environment property set object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Plug-ins can use this method to create an environment property set object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset">ITsSbEnvironmentPropertySet</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider">ITsSbProvider</a>
 

 

