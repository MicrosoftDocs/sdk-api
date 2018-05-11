---
UID: NF:wdstpdi.WdsTransportServerAllocateBuffer
title: WdsTransportServerAllocateBuffer function
author: windows-driver-content
description: Allocates a buffer in memory.
old-location: wds\wdstransportserverallocatebuffer.htm
old-project: Wds
ms.assetid: 0e227f46-a6f6-4fed-ac33-6e4e54f8b14d
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: WdsTransportServerAllocateBuffer, WdsTransportServerAllocateBuffer function [Windows Deployment Services], wds.wdstransportserverallocatebuffer, wdstpdi/WdsTransportServerAllocateBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdstpdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRANSPORTPROVIDER_CALLBACK_ID, *PTRANSPORTPROVIDER_CALLBACK_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wdsmc.dll
api_name:
-	WdsTransportServerAllocateBuffer
product: Windows
targetos: Windows
req.lib: Wdsmc.lib
req.dll: Wdsmc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WdsTransportServerAllocateBuffer function


## -description


Allocates a buffer in memory.


## -parameters




### -param hProvider [in]

Handle to the provider. This handle was given to the provider in the <a href="https://msdn.microsoft.com/b7592e8d-6d7d-426a-8520-7b9cc5810d5a">WdsTransportProviderInitialize</a> function. 


### -param ulBufferSize [in]

Size of the buffer to be allocated.

