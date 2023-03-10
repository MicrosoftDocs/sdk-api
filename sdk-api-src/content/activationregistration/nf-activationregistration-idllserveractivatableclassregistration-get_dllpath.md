---
UID: NF:activationregistration.IDllServerActivatableClassRegistration.get_DllPath
title: IDllServerActivatableClassRegistration::get_DllPath (activationregistration.h)
description: Gets the fully qualified path to the in-process server.
helpviewer_keywords: ["IDllServerActivatableClassRegistration interface [Windows Runtime]","get_DllPath method","IDllServerActivatableClassRegistration.get_DllPath","IDllServerActivatableClassRegistration::get_DllPath","activationregistration/IDllServerActivatableClassRegistration::get_DllPath","get_DllPath","get_DllPath method [Windows Runtime]","get_DllPath method [Windows Runtime]","IDllServerActivatableClassRegistration interface","winrt.idllserveractivatableclassregistration_dllpath"]
old-location: winrt\idllserveractivatableclassregistration_dllpath.htm
tech.root: WinRT
ms.assetid: B46BB464-C993-49A7-86C8-4945E69AA9CC
ms.date: 12/05/2018
ms.keywords: IDllServerActivatableClassRegistration interface [Windows Runtime],get_DllPath method, IDllServerActivatableClassRegistration.get_DllPath, IDllServerActivatableClassRegistration::get_DllPath, activationregistration/IDllServerActivatableClassRegistration::get_DllPath, get_DllPath, get_DllPath method [Windows Runtime], get_DllPath method [Windows Runtime],IDllServerActivatableClassRegistration interface, winrt.idllserveractivatableclassregistration_dllpath
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
 - IDllServerActivatableClassRegistration::get_DllPath
 - activationregistration/IDllServerActivatableClassRegistration::get_DllPath
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
 - IDllServerActivatableClassRegistration.get_DllPath
---

# IDllServerActivatableClassRegistration::get_DllPath


## -description

Gets the fully qualified path to the in-process server.

## -parameters

### -param dllPath [out, retval]

The fully qualified path to the in-process server.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/activationregistration/nn-activationregistration-idllserveractivatableclassregistration">IDllServerActivatableClassRegistration</a>