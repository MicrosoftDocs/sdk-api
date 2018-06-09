---
UID: NF:strmif.IVMRMixerControl.GetMixingPrefs
title: IVMRMixerControl::GetMixingPrefs
author: windows-sdk-content
description: Retrieves the mixing preferences for the stream.
old-location: dshow\ivmrmixercontrol_getmixingprefs.htm
old-project: DirectShow
ms.assetid: ee410a7e-e021-408a-bf40-cb58dc8eca1c
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetMixingPrefs, GetMixingPrefs method [DirectShow], GetMixingPrefs method [DirectShow],IVMRMixerControl interface, IVMRMixerControl interface [DirectShow],GetMixingPrefs method, IVMRMixerControl.GetMixingPrefs, IVMRMixerControl::GetMixingPrefs, IVMRMixerControlGetMixingPrefs, dshow.ivmrmixercontrol_getmixingprefs, strmif/IVMRMixerControl::GetMixingPrefs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRMixerControl.GetMixingPrefs
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRMixerControl::GetMixingPrefs


## -description



Retrieves the mixing preferences for the stream.




## -parameters




### -param pdwMixerPrefs






#### - dwMixerPrefs [in]

Address of a variable that receives a bitwise OR combination of <a href="https://msdn.microsoft.com/0852590c-6bca-4261-99c0-fff8a012f18e">VMRMixerPrefs</a> flags.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2aefaebc-14e7-4918-9256-c5e9e3449095">IVMRMixerControl Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

