---
UID: NF:activationregistration.IExeServerRegistration.get_AppUserModelId
title: IExeServerRegistration::get_AppUserModelId (activationregistration.h)
description: Gets the identifier for the app's user model.
helpviewer_keywords: ["IExeServerRegistration interface [Windows Runtime]","get_AppUserModelId method","IExeServerRegistration.get_AppUserModelId","IExeServerRegistration::get_AppUserModelId","activationregistration/IExeServerRegistration::get_AppUserModelId","get_AppUserModeId","get_AppUserModelId","get_AppUserModelId method [Windows Runtime]","get_AppUserModelId method [Windows Runtime]","IExeServerRegistration interface","winrt.iexeserverregistration_appusermodelid"]
old-location: winrt\iexeserverregistration_appusermodelid.htm
tech.root: WinRT
ms.assetid: DC0E3542-662F-43B8-968B-9F565D9D9278
ms.date: 12/05/2018
ms.keywords: IExeServerRegistration interface [Windows Runtime],get_AppUserModelId method, IExeServerRegistration.get_AppUserModelId, IExeServerRegistration::get_AppUserModelId, activationregistration/IExeServerRegistration::get_AppUserModelId, get_AppUserModeId, get_AppUserModelId, get_AppUserModelId method [Windows Runtime], get_AppUserModelId method [Windows Runtime],IExeServerRegistration interface, winrt.iexeserverregistration_appusermodelid
req.header: activationregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IExeServerRegistration::get_AppUserModelId
 - activationregistration/IExeServerRegistration::get_AppUserModelId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - activationregistration.h
api_name:
 - IExeServerRegistration.get_AppUserModelId
---

# IExeServerRegistration::get_AppUserModelId


## -description

Gets the identifier for the app's user model.

## -parameters

### -param appUserModelId [out, retval]

The identifier for the app's user model.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iexeserveractivatableclassregistration">IExeServerActivatableClassRegistration</a>



<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iexeserverregistration">IExeServerRegistration</a>