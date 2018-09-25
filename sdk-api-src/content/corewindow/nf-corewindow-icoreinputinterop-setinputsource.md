---
UID: NF:corewindow.ICoreInputInterop.SetInputSource
title: ICoreInputInterop::SetInputSource
author: windows-sdk-content
description: Sets the input source for an app's CoreIndependentInputSource or CoreComponentInputSource.
old-location: winrt\icoreinputinterop_setinputsource.htm
tech.root: WinRT
ms.assetid: 693180F5-2C19-47CD-9514-F0CEA1849A4A
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICoreInputInterop interface [Windows Runtime],SetInputSource method, ICoreInputInterop.SetInputSource, ICoreInputInterop::SetInputSource, SetInputSource, SetInputSource method [Windows Runtime], SetInputSource method [Windows Runtime],ICoreInputInterop interface, corewindow/ICoreInputInterop::SetInputSource, winrt.icoreinputinterop_setinputsource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: corewindow.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - corewindow.h
api_name:
 - ICoreInputInterop.SetInputSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICoreInputInterop::SetInputSource


## -description


Sets the input source for an app's <a href="https://msdn.microsoft.com/917cbf9f-bd19-4e05-bcd1-cf6a86f16e65">CoreIndependentInputSource</a> or <a href="https://msdn.microsoft.com/3075a07b-c432-482e-a44b-494014ff13fc">CoreComponentInputSource</a>.


## -parameters




### -param value [in]

Pointer to the base COM interface of the input source.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3075a07b-c432-482e-a44b-494014ff13fc">CoreComponentInputSource</a>



<a href="https://msdn.microsoft.com/917cbf9f-bd19-4e05-bcd1-cf6a86f16e65">CoreIndependentInputSource</a>



<a href="https://msdn.microsoft.com/F7BA7EFB-D9DC-4FF2-97A4-C4818BCBD599">ICoreInputInterop</a>
 

 

