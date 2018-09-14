---
UID: NF:sbtsv.ITsSbProvider.GetFilterPluginStore
title: ITsSbProvider::GetFilterPluginStore
author: windows-sdk-content
description: Retrieves a FilterPluginStore instance of the filter plugin store.
old-location: termserv\itssbprovider_getfilterpluginstore.htm
tech.root: TermServ
ms.assetid: 39ba9d60-7dde-4aa1-b95e-ec26aef731ca
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetFilterPluginStore, GetFilterPluginStore method [Remote Desktop Services], GetFilterPluginStore method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],GetFilterPluginStore method, ITsSbProvider.GetFilterPluginStore, ITsSbProvider::GetFilterPluginStore, sbtsv/ITsSbProvider::GetFilterPluginStore, termserv.itssbprovider_getfilterpluginstore
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITsSbProvider.GetFilterPluginStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbProvider::GetFilterPluginStore


## -description


Retrieves a <a href="https://msdn.microsoft.com/59541fc2-0063-41ca-bcfe-536bb1742c6e">FilterPluginStore</a> instance of the  filter plugin store.


## -parameters




### -param ppStore [out]

The address of an <a href="https://msdn.microsoft.com/59541fc2-0063-41ca-bcfe-536bb1742c6e">ITsSbFilterPluginStore</a> interface pointer.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a8574750-d86e-4b0d-a534-d005596e2a33">ITsSbProvider</a>
 

 

