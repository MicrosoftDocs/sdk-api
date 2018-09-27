---
UID: NS:mbnapi.MBN_PROVIDER2
title: MBN_PROVIDER2
author: windows-sdk-content
description: The MBN_PROVIDER2 structure represents a network service provider. It is used by many of the provider-specific methods of the IMbnMultiCarrier interface and provides an extension to MBN_PROVIDER to support multi-carrier.
old-location: mbn\mbn_provider2.htm
tech.root: mbn
ms.assetid: 9D681192-1E40-4314-8E7F-8934AA8162D3
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: MBN_PROVIDER2, MBN_PROVIDER2 structure [Microsoft Broadband Networks], mbn.mbn_provider2, mbnapi/MBN_PROVIDER2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_PROVIDER2
product: Windows
targetos: Windows
req.typenames: MBN_PROVIDER2
req.redist: 
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
 

 

