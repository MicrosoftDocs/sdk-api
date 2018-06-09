---
UID: NF:sbtsv.ITsSbProvider.CreateEnvironmentPropertySetObject
title: ITsSbProvider::CreateEnvironmentPropertySetObject
author: windows-sdk-content
description: Creates an ITsSbEnvironmentPropertySet environment property set object.
old-location: termserv\itssbprovider_createenvironmentpropertysetobject.htm
old-project: TermServ
ms.assetid: 52bb5c05-f8eb-42c9-862f-d42e71507a91
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CreateEnvironmentPropertySetObject, CreateEnvironmentPropertySetObject method [Remote Desktop Services], CreateEnvironmentPropertySetObject method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],CreateEnvironmentPropertySetObject method, ITsSbProvider.CreateEnvironmentPropertySetObject, ITsSbProvider::CreateEnvironmentPropertySetObject, sbtsv/ITsSbProvider::CreateEnvironmentPropertySetObject, termserv.itssbprovider_createenvironmentpropertysetobject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TS_SB_SORT_BY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbProvider.CreateEnvironmentPropertySetObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITsSbProvider::CreateEnvironmentPropertySetObject


## -description


Creates an <a href="https://msdn.microsoft.com/613c972d-ab52-495a-a8fd-2827e39e9a4e">ITsSbEnvironmentPropertySet</a> environment property set object.


## -parameters




### -param ppPropertySet [out]

A pointer to the created <a href="https://msdn.microsoft.com/613c972d-ab52-495a-a8fd-2827e39e9a4e">ITsSbEnvironmentPropertySet</a> environment property set object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Plug-ins can use this method to create an environment property set object.




## -see-also




<a href="https://msdn.microsoft.com/613c972d-ab52-495a-a8fd-2827e39e9a4e">ITsSbEnvironmentPropertySet</a>



<a href="https://msdn.microsoft.com/a8574750-d86e-4b0d-a534-d005596e2a33">ITsSbProvider</a>
 

 

