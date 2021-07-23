---
UID: NN:wbemprov.IWbemProviderIdentity
title: IWbemProviderIdentity (wbemprov.h)
description: The IWbemProviderIdentity interface is implemented by an event provider if the provider registers itself using more than one Name (multiple instances of __Win32Provider) with the same CLSID value.
helpviewer_keywords: ["IWbemProviderIdentity","IWbemProviderIdentity interface [Windows Management Instrumentation]","IWbemProviderIdentity interface [Windows Management Instrumentation]","described","_hmm_iwbemprovideridentity","wbemprov/IWbemProviderIdentity","wmi.iwbemprovideridentity"]
old-location: wmi\iwbemprovideridentity.htm
tech.root: wmi
ms.assetid: 872daa72-c6ff-4c6d-a870-c32e3688eb13
ms.date: 12/05/2018
ms.keywords: IWbemProviderIdentity, IWbemProviderIdentity interface [Windows Management Instrumentation], IWbemProviderIdentity interface [Windows Management Instrumentation],described, _hmm_iwbemprovideridentity, wbemprov/IWbemProviderIdentity, wmi.iwbemprovideridentity
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
 - IWbemProviderIdentity
 - wbemprov/IWbemProviderIdentity
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
 - IWbemProviderIdentity
---

# IWbemProviderIdentity interface


## -description

The 
<b>IWbemProviderIdentity</b> interface is implemented by an event provider if the provider registers itself using more than one 
<b>Name</b> (multiple instances of 
<a href="/windows/desktop/WmiSdk/--win32provider">__Win32Provider</a>) with the same <a href="/windows/desktop/com/clsid">CLSID</a> value. The class provides a mechanism for distinguishing which named provider should be used.

## -inheritance

The <b>IWbemProviderIdentity</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemProviderIdentity</b> also has these types of members:

