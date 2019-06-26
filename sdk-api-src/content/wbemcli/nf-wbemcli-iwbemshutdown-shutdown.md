---
UID: NF:wbemcli.IWbemShutdown.Shutdown
title: IWbemShutdown::Shutdown (wbemcli.h)
author: windows-sdk-content
description: The IWbemShutdown::Shutdown method indicates to the provider that the provider services are not required.
old-location: wmi\iwbemshutdown_shutdown.htm
tech.root: WmiSdk
ms.assetid: b6eb56ae-5869-413f-a455-22616b04c18f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWbemShutdown interface [Windows Management Instrumentation],Shutdown method, IWbemShutdown.Shutdown, IWbemShutdown::Shutdown, Shutdown, Shutdown method [Windows Management Instrumentation], Shutdown method [Windows Management Instrumentation],IWbemShutdown interface, wbemcli/IWbemShutdown::Shutdown, wmi.iwbemshutdown_shutdown
ms.topic: method
f1_keywords: 
 - "wbemcli/IWbemShutdown.Shutdown"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
api_name:
 - IWbemShutdown.Shutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemShutdown::Shutdown


## -description


The <b>IWbemShutdown::Shutdown</b> method indicates to the provider that the  provider services are not required.


## -parameters




### -param uReason [in]

Reserved. This value must be zero (0).


### -param uMaxMilliseconds [in]

Reserved. This value must be zero (0).


### -param pCtx [in]

Reserved. This value must be <b>NULL</b>.


## -returns



This method returns an <b>HRESULT</b>, which identifies the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemshutdown">IWbemShutdown</a>
 

 

