---
UID: NF:wmsdkidl.IWMVideoMediaProps.SetQuality
title: IWMVideoMediaProps::SetQuality
author: windows-sdk-content
description: The SetQuality method specifies the quality setting for the video stream.
old-location: wmformat\iwmvideomediaprops_setquality.htm
tech.root: wmformat
ms.assetid: 0f91380d-b8c8-47db-99ca-12c897bdff20
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMVideoMediaProps interface [windows Media Format],SetQuality method, IWMVideoMediaProps.SetQuality, IWMVideoMediaProps::SetQuality, IWMVideoMediaPropsSetQuality, SetQuality, SetQuality method [windows Media Format], SetQuality method [windows Media Format],IWMVideoMediaProps interface, wmformat.iwmvideomediaprops_setquality, wmsdkidl/IWMVideoMediaProps::SetQuality
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
req.lib: Wmvcore.lib
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
api_name:
 - IWMVideoMediaProps.SetQuality
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmsdkidl.h
: 
- IWMVideoMediaProps.SetQuality
: 
---

# IWMVideoMediaProps::SetQuality


## -description



The <b>SetQuality</b> method specifies the quality setting for the video stream.




## -parameters




### -param dwQuality [in]

<b>DWORD</b> specifying the quality setting, in the range from zero (maximum <a href="https://msdn.microsoft.com/en-us/library/Dd757828(v=VS.85).aspx">frame rate</a>) to 100 (maximum image quality).


## -returns



This method always returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/4d6ba1d8-b046-450b-a3f9-4810faba5b77">IWMVideoMediaProps Interface</a>



<a href="https://msdn.microsoft.com/9edfe229-ffc5-4266-93af-1938bbd577c2">IWMVideoMediaProps::GetQuality</a>
 

 

