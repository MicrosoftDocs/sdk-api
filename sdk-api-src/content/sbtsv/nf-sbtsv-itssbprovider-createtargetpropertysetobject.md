---
UID: NF:sbtsv.ITsSbProvider.CreateTargetPropertySetObject
title: ITsSbProvider::CreateTargetPropertySetObject (sbtsv.h)
description: Creates an ITsSbTargetPropertySet target property set object.
helpviewer_keywords: ["CreateTargetPropertySetObject","CreateTargetPropertySetObject method [Remote Desktop Services]","CreateTargetPropertySetObject method [Remote Desktop Services]","ITsSbProvider interface","ITsSbProvider interface [Remote Desktop Services]","CreateTargetPropertySetObject method","ITsSbProvider.CreateTargetPropertySetObject","ITsSbProvider::CreateTargetPropertySetObject","sbtsv/ITsSbProvider::CreateTargetPropertySetObject","termserv.itssbprovider_createtargetpropertysetobject"]
old-location: termserv\itssbprovider_createtargetpropertysetobject.htm
tech.root: TermServ
ms.assetid: 82e9d414-2137-44f3-a984-dc12aba3ecd9
ms.date: 12/05/2018
ms.keywords: CreateTargetPropertySetObject, CreateTargetPropertySetObject method [Remote Desktop Services], CreateTargetPropertySetObject method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],CreateTargetPropertySetObject method, ITsSbProvider.CreateTargetPropertySetObject, ITsSbProvider::CreateTargetPropertySetObject, sbtsv/ITsSbProvider::CreateTargetPropertySetObject, termserv.itssbprovider_createtargetpropertysetobject
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
 - ITsSbProvider::CreateTargetPropertySetObject
 - sbtsv/ITsSbProvider::CreateTargetPropertySetObject
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
 - ITsSbProvider.CreateTargetPropertySetObject
---

# ITsSbProvider::CreateTargetPropertySetObject


## -description

Creates an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtargetpropertyset">ITsSbTargetPropertySet</a> target property set object.

## -parameters

### -param ppPropertySet [out]

A pointer to a pointer to an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtargetpropertyset">ITsSbTargetPropertySet</a> property set object. When you have finished using the object, release it by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method. Because RD Connection Broker is unaware of the contents of the property set object, you should clean the object before calling its <b>Release</b> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Plug-ins can use this method to create a target property set object.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider">ITsSbProvider</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtargetpropertyset">ITsSbTargetPropertySet</a>