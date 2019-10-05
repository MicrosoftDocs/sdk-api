---
UID: NF:sbtsv.ITsSbProvider.GetResourcePluginStore
title: ITsSbProvider::GetResourcePluginStore (sbtsv.h)
author: windows-sdk-content
description: Retrieves an ITsSbResourcePluginStore instance of the resource plug-in store.
old-location: termserv\itssbprovider_getresourcepluginstore.htm
tech.root: TermServ
ms.assetid: 9e4d5b1d-100e-49e1-b1b5-4b126683c329
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetResourcePluginStore, GetResourcePluginStore method [Remote Desktop Services], GetResourcePluginStore method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],GetResourcePluginStore method, ITsSbProvider.GetResourcePluginStore, ITsSbProvider::GetResourcePluginStore, sbtsv/ITsSbProvider::GetResourcePluginStore, termserv.itssbprovider_getresourcepluginstore
ms.topic: method
f1_keywords: 
 - "sbtsv/ITsSbProvider.GetResourcePluginStore"
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
 - ITsSbProvider.GetResourcePluginStore
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbProvider::GetResourcePluginStore


## -description


Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a> instance of the resource plug-in store.

Plug-ins can call this method if they have access to the <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider">ITsSbProvider</a> and <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourceplugin">ITsSbResourcePlugin</a> objects that own the store. This method returns an instance of the resource plug-in store.


## -parameters




### -param ppStore [out]

A pointer to a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a> resource plug-in store object. When you have finished using the object, release it by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider">ITsSbProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourceplugin">ITsSbResourcePlugin</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>
 

 

