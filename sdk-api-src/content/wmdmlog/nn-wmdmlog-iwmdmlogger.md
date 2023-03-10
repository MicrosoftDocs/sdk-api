---
UID: NN:wmdmlog.IWMDMLogger
title: IWMDMLogger (wmdmlog.h)
description: The IWMDMLogger interface is used by Windows Media Device Manager applications and service providers to log entries in a common log file.
helpviewer_keywords: ["IWMDMLogger","IWMDMLogger interface [windows Media Device Manager]","IWMDMLogger interface [windows Media Device Manager]","described","IWMDMLoggerInterface","wmdm.iwmdmlogger","wmdmlog/IWMDMLogger"]
old-location: wmdm\iwmdmlogger.htm
tech.root: WMDM
ms.assetid: bededb91-f343-455b-a3ef-548e6f961933
ms.date: 12/05/2018
ms.keywords: IWMDMLogger, IWMDMLogger interface [windows Media Device Manager], IWMDMLogger interface [windows Media Device Manager],described, IWMDMLoggerInterface, wmdm.iwmdmlogger, wmdmlog/IWMDMLogger
req.header: wmdmlog.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IWMDMLogger
 - wmdmlog/IWMDMLogger
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmdmlog.h
api_name:
 - IWMDMLogger
---

# IWMDMLogger interface


## -description

The <b>IWMDMLogger</b> interface is used by Windows Media Device Manager applications and service providers to log entries in a common log file. Components do not need to be certified to use this object.

This interface is exposed by a COM object that must be created using the class ID CLSID_WMDMLogger, as shown here:


```cpp

IWMDMLogger* m_pLogger = NULL;
CoCreateInstance(CLSID_WMDMLogger, NULL, CLSCTX_ALL, __uuidof(IWMDMLogger), (void**)&m_pLogger);

```


This interface GUID is not properly defined in mssachlp.lib; therefore, to get the proper definitions when implementing this interface, you must #include both mswmdm.h and wmdmlog_i.c from wmdmlog.idl.

## -inheritance

The <b>IWMDMLogger</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMLogger</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WMDM/enabling-logging">Enabling Logging</a>



<a href="/windows/desktop/WMDM/interfaces-for-service-providers-and-applications">Interfaces for Service Providers and Applications</a>
