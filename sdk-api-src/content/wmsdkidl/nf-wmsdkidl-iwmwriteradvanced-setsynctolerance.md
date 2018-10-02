---
UID: NF:wmsdkidl.IWMWriterAdvanced.SetSyncTolerance
title: IWMWriterAdvanced::SetSyncTolerance
author: windows-sdk-content
description: The SetSyncTolerance method sets the amount of time that the inputs can fall out of synchronization before the samples are discarded.
old-location: wmformat\iwmwriteradvanced_setsynctolerance.htm
tech.root: wmformat
ms.assetid: d60020bf-52f1-46a0-aeae-367e3b179fac
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMWriterAdvanced interface [windows Media Format],SetSyncTolerance method, IWMWriterAdvanced.SetSyncTolerance, IWMWriterAdvanced::SetSyncTolerance, IWMWriterAdvancedSetSyncTolerance, SetSyncTolerance, SetSyncTolerance method [windows Media Format], SetSyncTolerance method [windows Media Format],IWMWriterAdvanced interface, wmformat.iwmwriteradvanced_setsynctolerance, wmsdkidl/IWMWriterAdvanced::SetSyncTolerance
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
 - IWMWriterAdvanced.SetSyncTolerance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterAdvanced::SetSyncTolerance


## -description



The <b>SetSyncTolerance</b> method sets the amount of time that the inputs can fall out of synchronization before the samples are discarded.




## -parameters




### -param msWindow [in]

Amount of time that the inputs can be out of synchronization, in milliseconds. Note that this parameter is in milliseconds and not 100-nanosecond units.


## -returns



This method always returns S_OK.




## -remarks



The default tolerance value is 3000 milliseconds.

Regardless of what the tolerance is set to, keeping samples as tightly synchronized as possible results in the best performance and the highest-quality content.




## -see-also




<a href="https://msdn.microsoft.com/082cd277-157d-42a4-bf37-e47d16f90c7a">IWMWriterAdvanced Interface</a>



<a href="https://msdn.microsoft.com/f62d3405-3125-4df6-bd06-fa70358560ad">IWMWriterAdvanced::GetSyncTolerance</a>
 

 

