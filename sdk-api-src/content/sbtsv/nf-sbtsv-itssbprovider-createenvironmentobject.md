---
UID: NF:sbtsv.ITsSbProvider.CreateEnvironmentObject
title: ITsSbProvider::CreateEnvironmentObject (sbtsv.h)
description: Creates an ITsSbEnvironment environment object.
helpviewer_keywords: ["CreateEnvironmentObject","CreateEnvironmentObject method [Remote Desktop Services]","CreateEnvironmentObject method [Remote Desktop Services]","ITsSbProvider interface","ITsSbProvider interface [Remote Desktop Services]","CreateEnvironmentObject method","ITsSbProvider.CreateEnvironmentObject","ITsSbProvider::CreateEnvironmentObject","sbtsv/ITsSbProvider::CreateEnvironmentObject","termserv.itssbprovider_createenvironmentobject"]
old-location: termserv\itssbprovider_createenvironmentobject.htm
tech.root: TermServ
ms.assetid: 11570f40-979e-4caf-81af-f8d16ec61391
ms.date: 12/05/2018
ms.keywords: CreateEnvironmentObject, CreateEnvironmentObject method [Remote Desktop Services], CreateEnvironmentObject method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],CreateEnvironmentObject method, ITsSbProvider.CreateEnvironmentObject, ITsSbProvider::CreateEnvironmentObject, sbtsv/ITsSbProvider::CreateEnvironmentObject, termserv.itssbprovider_createenvironmentobject
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
 - ITsSbProvider::CreateEnvironmentObject
 - sbtsv/ITsSbProvider::CreateEnvironmentObject
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
 - ITsSbProvider.CreateEnvironmentObject
---

# ITsSbProvider::CreateEnvironmentObject


## -description

Creates an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment">ITsSbEnvironment</a> environment object.

## -parameters

### -param Name [in]

A <b>BSTR</b> variable that contains the name of the object to create.

### -param ServerWeight [in]

A <b>DWORD</b> variable that contains the server weight of the object to create.

### -param ppEnvironment [out]

A pointer to a pointer to the newly created environment object. When you have finished using the object, release it by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method.

## -returns

This method can return one of these values.


If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list.

## -remarks

Plug-ins can use this method to create an environment object.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment">ITsSbEnvironment</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider">ITsSbProvider</a>