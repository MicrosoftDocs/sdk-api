---
UID: NF:sbtsv.ITsSbProvider.CreatePluginPropertySet
title: ITsSbProvider::CreatePluginPropertySet (sbtsv.h)
description: Creates an ITsSbPluginPropertySet plug-in property set object.
helpviewer_keywords: ["CreatePluginPropertySet","CreatePluginPropertySet method [Remote Desktop Services]","CreatePluginPropertySet method [Remote Desktop Services]","ITsSbProvider interface","ITsSbProvider interface [Remote Desktop Services]","CreatePluginPropertySet method","ITsSbProvider.CreatePluginPropertySet","ITsSbProvider::CreatePluginPropertySet","sbtsv/ITsSbProvider::CreatePluginPropertySet","termserv.itssbprovider_createpluginpropertyset"]
old-location: termserv\itssbprovider_createpluginpropertyset.htm
tech.root: TermServ
ms.assetid: a15edb7a-4ff5-4832-8632-17b08cff4675
ms.date: 12/05/2018
ms.keywords: CreatePluginPropertySet, CreatePluginPropertySet method [Remote Desktop Services], CreatePluginPropertySet method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],CreatePluginPropertySet method, ITsSbProvider.CreatePluginPropertySet, ITsSbProvider::CreatePluginPropertySet, sbtsv/ITsSbProvider::CreatePluginPropertySet, termserv.itssbprovider_createpluginpropertyset
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
 - ITsSbProvider::CreatePluginPropertySet
 - sbtsv/ITsSbProvider::CreatePluginPropertySet
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
 - ITsSbProvider.CreatePluginPropertySet
---

# ITsSbProvider::CreatePluginPropertySet


## -description

Creates an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginpropertyset">ITsSbPluginPropertySet</a> plug-in property set object.

## -parameters

### -param ppPropertySet [out, retval]

A pointer to a pointer to an 
<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginpropertyset">ITsSbPluginPropertySet</a> property set object. When you have finished 
using the object, release it by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method. 
Because RD Connection Broker is unaware of the contents of the property set object, you should clean the object before calling 
its <b>Release</b> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 Plug-ins can use this method to create a plug-in property set object.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginpropertyset">ITsSbPluginPropertySet</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider">ITsSbProvider</a>