---
UID: NF:mfidl.IMFSystemId.Setup
title: IMFSystemId::Setup
author: windows-sdk-content
description: Sets up the IMFSystemId.
old-location: mf\imfsystemid_setup.htm
tech.root: medfound
ms.assetid: 6a779581-326a-4666-8e11-d7cdcb02faa2
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IMFSystemId interface [Media Foundation],Setup method, IMFSystemId.Setup, IMFSystemId::Setup, Setup, Setup method [Media Foundation], Setup method [Media Foundation],IMFSystemId interface, mf.imfsystemid_setup, mfidl/IMFSystemId::Setup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFSystemId.Setup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSystemId::Setup


## -description


Sets up the <a href="https://msdn.microsoft.com/45c80fc5-5ea7-4d4e-9c9c-5a38f62b2d28">IMFSystemId</a>.


## -parameters




### -param stage

Stage in the setup process. 0 or 1.


### -param cbIn

Size of the input buffer.


### -param pbIn

The input buffer.


### -param pcbOut

Size of output buffer.


### -param ppbOut

The output buffer.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/45c80fc5-5ea7-4d4e-9c9c-5a38f62b2d28">IMFSystemId</a>
 

 

