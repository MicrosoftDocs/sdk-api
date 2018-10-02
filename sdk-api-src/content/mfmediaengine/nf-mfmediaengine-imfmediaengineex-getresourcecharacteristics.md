---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetResourceCharacteristics
title: IMFMediaEngineEx::GetResourceCharacteristics
author: windows-sdk-content
description: Gets various flags that describe the media resource.
old-location: mf\imfmediaengineex_getresourcecharacteristics.htm
tech.root: MedFound
ms.assetid: 534595D7-007F-450B-A1C7-FA08F3958417
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetResourceCharacteristics, GetResourceCharacteristics method [Media Foundation], GetResourceCharacteristics method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetResourceCharacteristics method, IMFMediaEngineEx.GetResourceCharacteristics, IMFMediaEngineEx::GetResourceCharacteristics, mf.imfmediaengineex_getresourcecharacteristics, mfmediaengine/IMFMediaEngineEx::GetResourceCharacteristics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx.GetResourceCharacteristics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineEx::GetResourceCharacteristics


## -description


Gets various flags that describe the media resource.


## -parameters




### -param pCharacteristics [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/115f4a6b-99c2-436e-9483-c44003e61a7d">MFMEDIASOURCE_CHARACTERISTICS enumeration</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

