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

# IRawCDImageCreator::put_DisableGaplessAudio


## -description


Sets the value that specifies if "Gapless Audio" recording is disabled. This property defaults to a value of  <b>VARIANT_FALSE</b>, which disables the use of "gapless" recording between consecutive audio tracks.


## -parameters




### -param value

A <b>VARIANT_BOOL</b> value that specifies if "Gapless Audio" is disabled. Setting a value of <b>VARIANT_FALSE</b> disables "Gapless Audio", while <b>VARIANT_TRUE</b> enables it.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



When disabled, by default, the audio tracks will have the standard 2-second (150 sector) silent gap between tracks.  When enabled, the last 2  seconds of audio data from the previous audio track are encoded in the pregap area of the next audio track, enabling seamless transitions between tracks.

It is recommended that this property value is only set before the process of adding tracks to the image has begun as any changes afterwards could result in adverse effects to other image properties.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/b5fe1a32-545e-417d-9996-34d12862a0ea">IRawCDImageCreator</a>



<a href="https://msdn.microsoft.com/5f3bf774-3e09-40e9-bc0b-f33bfd046a51">IRawCDImageCreator::get_DisableGaplessAudio</a>
 

 

