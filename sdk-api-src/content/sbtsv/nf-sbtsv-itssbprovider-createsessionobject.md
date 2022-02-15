---
UID: NF:sbtsv.ITsSbProvider.CreateSessionObject
title: ITsSbProvider::CreateSessionObject (sbtsv.h)
description: Plug-ins can use the CreateSessionObject method to create an ITsSbSession session object.
helpviewer_keywords: ["CreateSessionObject","CreateSessionObject method [Remote Desktop Services]","CreateSessionObject method [Remote Desktop Services]","ITsSbProvider interface","ITsSbProvider interface [Remote Desktop Services]","CreateSessionObject method","ITsSbProvider.CreateSessionObject","ITsSbProvider::CreateSessionObject","sbtsv/ITsSbProvider::CreateSessionObject","termserv.itssbprovider_createsessionobject"]
old-location: termserv\itssbprovider_createsessionobject.htm
tech.root: TermServ
ms.assetid: 14c800f8-a3d6-4d12-b568-94ef2d8e0aaf
ms.date: 12/05/2018
ms.keywords: CreateSessionObject, CreateSessionObject method [Remote Desktop Services], CreateSessionObject method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],CreateSessionObject method, ITsSbProvider.CreateSessionObject, ITsSbProvider::CreateSessionObject, sbtsv/ITsSbProvider::CreateSessionObject, termserv.itssbprovider_createsessionobject
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
 - ITsSbProvider::CreateSessionObject
 - sbtsv/ITsSbProvider::CreateSessionObject
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
 - ITsSbProvider.CreateSessionObject
---

# ITsSbProvider::CreateSessionObject


## -description

Plug-ins can use the <b>CreateSessionObject</b> method to create an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession">ITsSbSession</a> session object.

## -parameters

### -param TargetName [in]

A <b>BSTR</b> variable that contains the target name.

### -param UserName [in]

A <b>BSTR</b> variable that contains the user name.

### -param Domain [in]

A <b>BSTR</b> variable that contains the domain.

### -param SessionId [in]

A <b>DWORD</b> variable that contains the session ID.

### -param ppSession [out]

A pointer to a pointer to the new session object. When you have finished using the object, release it by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider">ITsSbProvider</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession">ITsSbSession</a>