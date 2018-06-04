---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# MBN_PROVIDER2 structure


## -description


The <b>MBN_PROVIDER2</b> structure represents a network service provider. It is used by many of the provider-specific methods of the <a href="https://msdn.microsoft.com/E40517CE-3169-4F20-A572-EDBC8FEC2862">IMbnMultiCarrier</a> interface and provides an extension to <a href="https://msdn.microsoft.com/f4a02ca2-6be4-4843-a657-5d5dde8be623">MBN_PROVIDER</a> to support multi-carrier. This extension contains the signal strength of each provider, which helps to determine which provider a user should connect to.


## -struct-fields




### -field provider

Contains a single-carrier <a href="https://msdn.microsoft.com/f4a02ca2-6be4-4843-a657-5d5dde8be623">MBN_PROVIDER</a> structure.


### -field cellularClass

Contains a <a href="https://msdn.microsoft.com/2d75c20b-1ae4-4824-8918-41c20327a007">MBN_CELLULAR_CLASS</a> that specifies which cellular class the provider uses.


### -field signalStrength

 


### -field signalError

 




#### - SignalError

Contains the signal error rate as defined by <a href="https://msdn.microsoft.com/028adb54-9c81-4a5b-85f7-5c12ce8d84e4">GetSignalError</a>.


#### - SignalStrength

Contains the signal quality received by the device as defined by <a href="https://msdn.microsoft.com/9a580232-4cd2-42f4-a6c7-f777d78241b6">GetSignalStrength</a>.


## -see-also




<a href="https://msdn.microsoft.com/f4a02ca2-6be4-4843-a657-5d5dde8be623">MBN_PROVIDER</a>
 

 

