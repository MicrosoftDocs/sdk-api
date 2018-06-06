---
UID: NF:imapi2.IRawCDImageCreator.put_DisableGaplessAudio
title: IRawCDImageCreator::put_DisableGaplessAudio
author: windows-sdk-content
description: Sets the value that specifies if &#0034;Gapless Audio&#0034; recording is disabled. This property defaults to a value of VARIANT_FALSE, which disables the use of &#0034;gapless&#0034; recording between consecutive audio tracks.
old-location: imapi\irawcdimagecreator_put_disablegaplessaudio.htm
old-project: imapi
ms.assetid: c9e17ed7-f51a-4b28-82db-36cad1aedd39
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],put_DisableGaplessAudio method, IRawCDImageCreator.put_DisableGaplessAudio, IRawCDImageCreator::put_DisableGaplessAudio, imapi.irawcdimagecreator_put_disablegaplessaudio, imapi2/IRawCDImageCreator::put_DisableGaplessAudio, put_DisableGaplessAudio, put_DisableGaplessAudio method [IMAPI], put_DisableGaplessAudio method [IMAPI],IRawCDImageCreator interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IRawCDImageCreator.put_DisableGaplessAudio
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

