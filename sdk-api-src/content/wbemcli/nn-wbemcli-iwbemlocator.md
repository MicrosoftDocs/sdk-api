---
UID: NN:wbemcli.IWbemLocator
title: IWbemLocator (wbemcli.h)
description: Use the IWbemLocator interface to obtain the initial namespace pointer to the IWbemServices interface for WMI on a specific host computer.
helpviewer_keywords: ["IWbemLocator","IWbemLocator interface [Windows Management Instrumentation]","IWbemLocator interface [Windows Management Instrumentation]","described","_hmm_iwbemlocator","wbemcli/IWbemLocator","wmi.iwbemlocator"]
old-location: wmi\iwbemlocator.htm
tech.root: wmi
ms.assetid: 3e630987-82e3-4eb0-aec0-30562bc7c843
ms.date: 12/05/2018
ms.keywords: IWbemLocator, IWbemLocator interface [Windows Management Instrumentation], IWbemLocator interface [Windows Management Instrumentation],described, _hmm_iwbemlocator, wbemcli/IWbemLocator, wmi.iwbemlocator
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wbemcli.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Wbemcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemLocator
 - wbemcli/IWbemLocator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemcore.dll
api_name:
 - IWbemLocator
---

# IWbemLocator interface


## -description

Use the 
<b>IWbemLocator</b> interface to obtain the initial namespace pointer to the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> interface for WMI on a specific host computer. You can access Windows Management itself using the 
<b>IWbemServices</b> pointer, which is returned by the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemlocator-connectserver">IWbemLocator::ConnectServer</a> method.

A client or provider that requires Windows Management services first obtains a pointer to the locator using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a>, as specified in the COM documentation in the Microsoft Windows Software Development Kit (SDK). The 
<b>IWbemLocator</b> object is always an in-process COM server. The interface pointer to the desired namespace on the desired target computer is then obtained through the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemlocator-connectserver">IWbemLocator::ConnectServer</a> method, which is the only method on this interface.

## -inheritance

The <b>IWbemLocator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemLocator</b> also has these types of members:

