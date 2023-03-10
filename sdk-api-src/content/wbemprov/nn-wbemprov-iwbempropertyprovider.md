---
UID: NN:wbemprov.IWbemPropertyProvider
title: IWbemPropertyProvider (wbemprov.h)
description: Supports retrieving and updating individual properties in an instance of a WMI class.
helpviewer_keywords: ["IWbemPropertyProvider","IWbemPropertyProvider interface [Windows Management Instrumentation]","IWbemPropertyProvider interface [Windows Management Instrumentation]","described","_hmm_iwbempropertyprovider","wbemprov/IWbemPropertyProvider","wmi.iwbempropertyprovider"]
old-location: wmi\iwbempropertyprovider.htm
tech.root: wmi
ms.assetid: 8a7910ae-4258-4486-80ff-82b1081083cc
ms.date: 12/05/2018
ms.keywords: IWbemPropertyProvider, IWbemPropertyProvider interface [Windows Management Instrumentation], IWbemPropertyProvider interface [Windows Management Instrumentation],described, _hmm_iwbempropertyprovider, wbemprov/IWbemPropertyProvider, wmi.iwbempropertyprovider
req.header: wbemprov.h
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
req.dll: Wbemsvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemPropertyProvider
 - wbemprov/IWbemPropertyProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemPropertyProvider
---

# IWbemPropertyProvider interface


## -description

The 
<b>IWbemPropertyProvider</b> interface supports retrieving and updating individual properties in an instance of a WMI class.<b>IWbemPropertyProvider</b> is the primary interface of property providers that supply dynamic data, which is the majority of property providers.  WMI is the only client of this interface, and it calls the methods whenever the properties are required by a client application of WMI.

## -inheritance

The <b>IWbemPropertyProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemPropertyProvider</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>
