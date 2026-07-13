---
UID: NF:activationregistration.IExeServerRegistration.get_ServerName
title: IExeServerRegistration::get_ServerName (activationregistration.h)
description: Gets the name of the current out-of-process server.
helpviewer_keywords: ["IExeServerRegistration interface [Windows Runtime]","get_ServerName method","IExeServerRegistration.get_ServerName","IExeServerRegistration::get_ServerName","activationregistration/IExeServerRegistration::get_ServerName","get_ServerName","get_ServerName method [Windows Runtime]","get_ServerName method [Windows Runtime]","IExeServerRegistration interface","winrt.iexeserverregistration_servername"]
old-location: winrt\iexeserverregistration_servername.htm
tech.root: WinRT
ms.assetid: CB7CAA65-4DA9-4948-AEB4-150A45629947
ms.date: 12/05/2018
ms.keywords: IExeServerRegistration interface [Windows Runtime],get_ServerName method, IExeServerRegistration.get_ServerName, IExeServerRegistration::get_ServerName, activationregistration/IExeServerRegistration::get_ServerName, get_ServerName, get_ServerName method [Windows Runtime], get_ServerName method [Windows Runtime],IExeServerRegistration interface, winrt.iexeserverregistration_servername
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
 - IExeServerRegistration::get_ServerName
 - activationregistration/IExeServerRegistration::get_ServerName
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
 - IExeServerRegistration.get_ServerName
---

# IExeServerRegistration::get_ServerName


## -description

Gets the name of the current out-of-process server.

## -parameters

### -param serverName [out, retval]

The name of the out-of-process server.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iexeserveractivatableclassregistration">IExeServerActivatableClassRegistration</a>



<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iexeserverregistration">IExeServerRegistration</a>