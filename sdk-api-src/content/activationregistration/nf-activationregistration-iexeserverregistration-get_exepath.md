---
UID: NF:activationregistration.IExeServerRegistration.get_ExePath
title: IExeServerRegistration::get_ExePath (activationregistration.h)
description: Gets the file path to the out-of-process server.
helpviewer_keywords: ["IExeServerRegistration interface [Windows Runtime]","get_ExePath method","IExeServerRegistration.get_ExePath","IExeServerRegistration::get_ExePath","activationregistration/IExeServerRegistration::get_ExePath","get_ExePath","get_ExePath method [Windows Runtime]","get_ExePath method [Windows Runtime]","IExeServerRegistration interface","winrt.iexeserverregistration_exepath"]
old-location: winrt\iexeserverregistration_exepath.htm
tech.root: WinRT
ms.assetid: 69E8D576-B842-4CD4-8D93-87E4E08D11CA
ms.date: 12/05/2018
ms.keywords: IExeServerRegistration interface [Windows Runtime],get_ExePath method, IExeServerRegistration.get_ExePath, IExeServerRegistration::get_ExePath, activationregistration/IExeServerRegistration::get_ExePath, get_ExePath, get_ExePath method [Windows Runtime], get_ExePath method [Windows Runtime],IExeServerRegistration interface, winrt.iexeserverregistration_exepath
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
 - IExeServerRegistration::get_ExePath
 - activationregistration/IExeServerRegistration::get_ExePath
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
 - IExeServerRegistration.get_ExePath
---

# IExeServerRegistration::get_ExePath


## -description

Gets the file path to the out-of-process server.

## -parameters

### -param exePath [out, retval]

The file path to the out-of-process server.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iexeserveractivatableclassregistration">IExeServerActivatableClassRegistration</a>



<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iexeserverregistration">IExeServerRegistration</a>