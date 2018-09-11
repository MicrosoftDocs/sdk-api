---
UID: NF:wmnetsourcecreator.INSNetSourceCreator.Shutdown
title: INSNetSourceCreator::Shutdown
author: windows-sdk-content
description: The Shutdown method properly disposes of all allocated memory used by the network source creator. You must call this method when you are finished using the network source creator, to ensure that all resources are released.
old-location: wmformat\insnetsourcecreator_shutdown.htm
tech.root: wmformat
ms.assetid: 746b2ffa-c5bc-4df0-84fd-c3f1395e0d3e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: INSNetSourceCreator interface [windows Media Format],Shutdown method, INSNetSourceCreator.Shutdown, INSNetSourceCreator::Shutdown, INSNetSourceCreatorShutdown, Shutdown, Shutdown method [windows Media Format], Shutdown method [windows Media Format],INSNetSourceCreator interface, wmformat.insnetsourcecreator_shutdown, wmnetsourcecreator/INSNetSourceCreator::Shutdown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmnetsourcecreator.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - INSNetSourceCreator.Shutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INSNetSourceCreator::Shutdown


## -description



The <b>Shutdown</b> method properly disposes of all allocated memory used by the network source creator. You must call this method when you are finished using the network source creator, to ensure that all resources are released.




## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/39e692a6-fb68-447f-bd28-8d216776157a">INSNetSourceCreator Interface</a>



<a href="https://msdn.microsoft.com/53c1a15e-3ced-44e5-b512-b381ae11aa65">INSNetSourceCreator::Initialize</a>
 

 

