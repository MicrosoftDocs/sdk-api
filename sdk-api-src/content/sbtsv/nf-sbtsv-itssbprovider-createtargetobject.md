---
UID: NF:sbtsv.ITsSbProvider.CreateTargetObject
title: ITsSbProvider::CreateTargetObject (sbtsv.h)
description: Creates an ITsSbTarget target object.
helpviewer_keywords: ["CreateTargetObject","CreateTargetObject method [Remote Desktop Services]","CreateTargetObject method [Remote Desktop Services]","ITsSbProvider interface","ITsSbProvider interface [Remote Desktop Services]","CreateTargetObject method","ITsSbProvider.CreateTargetObject","ITsSbProvider::CreateTargetObject","sbtsv/ITsSbProvider::CreateTargetObject","termserv.itssbprovider_createtargetobject"]
old-location: termserv\itssbprovider_createtargetobject.htm
tech.root: TermServ
ms.assetid: 9ee426a3-03fa-4535-84b6-f965bd9eba60
ms.date: 12/05/2018
ms.keywords: CreateTargetObject, CreateTargetObject method [Remote Desktop Services], CreateTargetObject method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],CreateTargetObject method, ITsSbProvider.CreateTargetObject, ITsSbProvider::CreateTargetObject, sbtsv/ITsSbProvider::CreateTargetObject, termserv.itssbprovider_createtargetobject
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
 - ITsSbProvider::CreateTargetObject
 - sbtsv/ITsSbProvider::CreateTargetObject
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
 - ITsSbProvider.CreateTargetObject
---

# ITsSbProvider::CreateTargetObject


## -description

Creates an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a> target object.

## -parameters

### -param TargetName [in]

A <b>BSTR</b> variable that contains the target name.

### -param EnvironmentName

A <b>BSTR</b> variable that contains the environment name.

### -param ppTarget [out]

A pointer to a pointer to the specified target object. When you have finished using the object, release it by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method.

## -returns

This method can return one of these values.


If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list.

## -remarks

Plug-ins can use this method to create a target object.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider">ITsSbProvider</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a>