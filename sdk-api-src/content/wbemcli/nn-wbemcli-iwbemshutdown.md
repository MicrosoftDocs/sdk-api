---
UID: NN:wbemcli.IWbemShutdown
title: IWbemShutdown
author: windows-sdk-content
description: The IWbemShutdown interface indicates to the provider that an instance of an object is ready to be discarded. The provider can use this call to release resources that it is referencing currently.
old-location: wmi\iwbemshutdown.htm
old-project: WmiSdk
ms.assetid: a228ed61-1f16-45f4-85f2-85661ce06b72
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: IWbemShutdown, IWbemShutdown interface [Windows Management Instrumentation], IWbemShutdown interface [Windows Management Instrumentation],described, wbemcli/ IWbemShutdown, wmi.iwbemshutdown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: WMI_OBJ_TEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fastprox.dll
api_name:
-	IWbemShutdown
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemShutdown interface


## -description


The <b>IWbemShutdown</b> interface indicates to the provider that an instance of an object is ready to be discarded. The provider can use this call to release resources that it is referencing currently.

The interface is used by providers to receive notification that their object implementation is no longer required.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">  IWbemShutdown</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>  IWbemShutdown</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>  IWbemShutdown</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a>
</td>
<td align="left" width="63%">
Indicates to a provider that the services provided by the provider are no longer required.

</td>
</tr>
</table> 

