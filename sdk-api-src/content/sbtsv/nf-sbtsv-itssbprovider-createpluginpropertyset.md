---
UID: NF:sbtsv.ITsSbProvider.CreatePluginPropertySet
title: ITsSbProvider::CreatePluginPropertySet (sbtsv.h)
author: windows-sdk-content
description: Creates an ITsSbPluginPropertySet plug-in property set object.
old-location: termserv\itssbprovider_createpluginpropertyset.htm
tech.root: TermServ
ms.assetid: a15edb7a-4ff5-4832-8632-17b08cff4675
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreatePluginPropertySet, CreatePluginPropertySet method [Remote Desktop Services], CreatePluginPropertySet method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],CreatePluginPropertySet method, ITsSbProvider.CreatePluginPropertySet, ITsSbProvider::CreatePluginPropertySet, sbtsv/ITsSbProvider::CreatePluginPropertySet, termserv.itssbprovider_createpluginpropertyset
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
 - ITsSbProvider.CreatePluginPropertySet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbProvider::CreatePluginPropertySet


## -description


Creates an <a href="https://msdn.microsoft.com/e28e4ce7-1d11-483e-b666-69b3c0ba34b1">ITsSbPluginPropertySet</a> plug-in property set object.


## -parameters




### -param ppPropertySet [out, retval]

A pointer to a pointer to an 
<a href="https://msdn.microsoft.com/e28e4ce7-1d11-483e-b666-69b3c0ba34b1">ITsSbPluginPropertySet</a> property set object. When you have finished 
using the object, release it by calling the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method. 
Because RD Connection Broker is unaware of the contents of the property set object, you should clean the object before calling 
its <b>Release</b> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 Plug-ins can use this method to create a plug-in property set object.




## -see-also




<a href="https://msdn.microsoft.com/e28e4ce7-1d11-483e-b666-69b3c0ba34b1">ITsSbPluginPropertySet</a>



<a href="https://msdn.microsoft.com/a8574750-d86e-4b0d-a534-d005596e2a33">ITsSbProvider</a>
 

 

