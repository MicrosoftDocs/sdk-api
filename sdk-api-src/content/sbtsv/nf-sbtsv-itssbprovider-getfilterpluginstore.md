---
UID: NF:sbtsv.ITsSbProvider.GetFilterPluginStore
title: ITsSbProvider::GetFilterPluginStore (sbtsv.h)
description: Retrieves a FilterPluginStore instance of the filter plugin store.
helpviewer_keywords: ["GetFilterPluginStore","GetFilterPluginStore method [Remote Desktop Services]","GetFilterPluginStore method [Remote Desktop Services]","ITsSbProvider interface","ITsSbProvider interface [Remote Desktop Services]","GetFilterPluginStore method","ITsSbProvider.GetFilterPluginStore","ITsSbProvider::GetFilterPluginStore","sbtsv/ITsSbProvider::GetFilterPluginStore","termserv.itssbprovider_getfilterpluginstore"]
old-location: termserv\itssbprovider_getfilterpluginstore.htm
tech.root: TermServ
ms.assetid: 39ba9d60-7dde-4aa1-b95e-ec26aef731ca
ms.date: 12/05/2018
ms.keywords: GetFilterPluginStore, GetFilterPluginStore method [Remote Desktop Services], GetFilterPluginStore method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],GetFilterPluginStore method, ITsSbProvider.GetFilterPluginStore, ITsSbProvider::GetFilterPluginStore, sbtsv/ITsSbProvider::GetFilterPluginStore, termserv.itssbprovider_getfilterpluginstore
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbProvider::GetFilterPluginStore
 - sbtsv/ITsSbProvider::GetFilterPluginStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbProvider.GetFilterPluginStore
---

# ITsSbProvider::GetFilterPluginStore


## -description

Retrieves a <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbfilterpluginstore">FilterPluginStore</a> instance of the  filter plugin store.

## -parameters

### -param ppStore [out]

The address of an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbfilterpluginstore">ITsSbFilterPluginStore</a> interface pointer.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider">ITsSbProvider</a>