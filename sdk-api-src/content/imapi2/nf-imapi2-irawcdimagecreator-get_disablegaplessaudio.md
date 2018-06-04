---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IRawCDImageCreator::get_DisableGaplessAudio


## -description


Retrieves the current value that specifies if "Gapless Audio" recording is disabled. This property defaults to a value of  <b>VARIANT_FALSE</b>, which disables the use of "gapless" recording between consecutive audio tracks.


## -parameters




### -param value [out]

A <b>VARIANT_BOOL</b> value that specifies if "Gapless Audio" is disabled. A value of <b>VARIANT_FALSE</b> indicates that "Gapless Audio" is disabled; <b>VARIANT_TRUE</b> indicates that it is enabled.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



When disabled, by default, the audio tracks will have the standard 2-second (150 sector) silent gap between tracks.  When enabled, the last 2  seconds of audio data from the previous audio track are encoded in the pregap area of the next audio track, enabling seamless transitions between tracks.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/b5fe1a32-545e-417d-9996-34d12862a0ea">IRawCDImageCreator</a>



<a href="https://msdn.microsoft.com/c9e17ed7-f51a-4b28-82db-36cad1aedd39">IRawCDImageCreator::put_DisableGaplessAudio</a>
 

 

