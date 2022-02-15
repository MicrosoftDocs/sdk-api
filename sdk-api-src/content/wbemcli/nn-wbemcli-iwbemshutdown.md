---
UID: NN:wbemcli.IWbemShutdown
title: IWbemShutdown (wbemcli.h)
description: The IWbemShutdown interface indicates to the provider that an instance of an object is ready to be discarded. The provider can use this call to release resources that it is referencing currently.
helpviewer_keywords: ["IWbemShutdown","IWbemShutdown interface [Windows Management Instrumentation]","IWbemShutdown interface [Windows Management Instrumentation]","described","wbemcli/ IWbemShutdown","wmi.iwbemshutdown"]
old-location: wmi\iwbemshutdown.htm
tech.root: wmi
ms.assetid: a228ed61-1f16-45f4-85f2-85661ce06b72
ms.date: 12/05/2018
ms.keywords: IWbemShutdown, IWbemShutdown interface [Windows Management Instrumentation], IWbemShutdown interface [Windows Management Instrumentation],described, wbemcli/ IWbemShutdown, wmi.iwbemshutdown
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemShutdown
 - wbemcli/IWbemShutdown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
api_name:
 - IWbemShutdown
---

# IWbemShutdown interface


## -description

The <b>IWbemShutdown</b> interface indicates to the provider that an instance of an object is ready to be discarded. The provider can use this call to release resources that it is referencing currently.

The interface is used by providers to receive notification that their object implementation is no longer required.

## -inheritance

The <b>  IWbemShutdown</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>  IWbemShutdown</b> also has these types of members:

