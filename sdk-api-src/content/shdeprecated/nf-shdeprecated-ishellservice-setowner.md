---
UID: NF:shdeprecated.IShellService.SetOwner
title: IShellService::SetOwner (shdeprecated.h)
description: Deprecated. Declares an owner reference to the service object.
helpviewer_keywords: ["IShellService interface [Windows Shell]","SetOwner method","IShellService.SetOwner","IShellService::SetOwner","SetOwner","SetOwner method [Windows Shell]","SetOwner method [Windows Shell]","IShellService interface","shdeprecated/IShellService::SetOwner","shell.IShellService_SetOwner","zone_IShellService_SetOwner"]
old-location: shell\IShellService_SetOwner.htm
tech.root: shell
ms.assetid: ef3865b2-b651-4072-86f2-2996fce061a4
ms.date: 12/05/2018
ms.keywords: IShellService interface [Windows Shell],SetOwner method, IShellService.SetOwner, IShellService::SetOwner, SetOwner, SetOwner method [Windows Shell], SetOwner method [Windows Shell],IShellService interface, shdeprecated/IShellService::SetOwner, shell.IShellService_SetOwner, zone_IShellService_SetOwner
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IShellService::SetOwner
 - shdeprecated/IShellService::SetOwner
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IShellService.SetOwner
---

# IShellService::SetOwner


## -description

Deprecated. Declares an owner reference to the service object.

## -parameters

### -param punkOwner

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

The address of an interface pointer to the owner object. If <b>NULL</b>, the object should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release the existing reference.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The client calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> for <a href="/windows/desktop/api/shdeprecated/nn-shdeprecated-ishellservice">IShellService</a>, then calls <b>SetOwner(this)</b> to declare ownership. When the client is dismissed, typically when the window is closed, it calls <b>SetOwner(NULL)</b> to instruct the service object to release the reference to the owner object.