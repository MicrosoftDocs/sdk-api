---
UID: NN:functiondiscoveryprovider.IFunctionDiscoveryServiceProvider
title: IFunctionDiscoveryServiceProvider
author: windows-sdk-content
description: This interface is implemented to create and initialize objects to provide a specified access interface to a resource represented by the function instance. After the object is created, the Initialize method is called to initialize the object.
old-location: ncd\ifunctiondiscoveryserviceprovider.htm
old-project: fundisc
ms.assetid: dbdf27dc-5fb9-49ef-9a9b-ffcd7b148479
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IFunctionDiscoveryServiceProvider, IFunctionDiscoveryServiceProvider interface, IFunctionDiscoveryServiceProvider interface,described, functiondiscoveryprovider/IFunctionDiscoveryServiceProvider, ncd.ifunctiondiscoveryserviceprovider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: functiondiscoveryprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryProvider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PropertyConstraint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunctionDiscoveryProvider.h
api_name:
 - IFunctionDiscoveryServiceProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IFunctionDiscoveryServiceProvider interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface is implemented to create and initialize objects to provide a specified access interface to a resource represented by the function instance. After the object is created, the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method is called to initialize the object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFunctionDiscoveryServiceProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFunctionDiscoveryServiceProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFunctionDiscoveryServiceProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an object that provides a specific interface that has been bound to the resource represented by the function instance.

</td>
</tr>
</table> 

