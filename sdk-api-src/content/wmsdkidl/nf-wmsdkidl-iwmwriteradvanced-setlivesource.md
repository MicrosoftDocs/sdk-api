---
UID: NF:wmsdkidl.IWMWriterAdvanced.SetLiveSource
title: IWMWriterAdvanced::SetLiveSource
author: windows-sdk-content
description: The SetLiveSource method sets a flag indicating whether the source is live.
old-location: wmformat\iwmwriteradvanced_setlivesource.htm
old-project: wmformat
ms.assetid: ab015f92-498e-44c7-95c9-869dfdfccc09
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMWriterAdvanced interface [windows Media Format],SetLiveSource method, IWMWriterAdvanced.SetLiveSource, IWMWriterAdvanced::SetLiveSource, IWMWriterAdvancedSetLiveSource, SetLiveSource, SetLiveSource method [windows Media Format], SetLiveSource method [windows Media Format],IWMWriterAdvanced interface, wmformat.iwmwriteradvanced_setlivesource, wmsdkidl/IWMWriterAdvanced::SetLiveSource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.redist: 
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
tech.root: 
req.typenames: WM_AETYPE
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
 - IWMWriterAdvanced.SetLiveSource
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterAdvanced::SetLiveSource


## -description



The <b>SetLiveSource</b> method sets a flag indicating whether the source is live.




## -parameters




### -param fIsLiveSource [in]

Boolean value that is True if the source is live.


## -returns



This method always returns S_OK.




## -remarks



The default is False. To handle incoming samples correctly, the writer object must be notified whether the source is live.




## -see-also




<a href="https://msdn.microsoft.com/082cd277-157d-42a4-bf37-e47d16f90c7a">IWMWriterAdvanced Interface</a>
 

 

