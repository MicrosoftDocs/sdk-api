---
UID: NF:baseaudioprocessingobject.AERT_Free
title: AERT_Free function
author: windows-sdk-content
description: The AERT_Free utility function releases (frees) memory that was locked by the AERT_Allocate function, for use by audio processing objects to process audio data.
old-location: audio\aert_free.htm
tech.root: audio
ms.assetid: 9a7506fa-a52d-42f5-9144-751de19123d5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AERT_Free, AERT_Free function [Audio Devices], audio.aert_free, audio_syseffects_r_d23cc22f-79bc-4772-90bb-edb1c3afa9a7.xml, baseaudioprocessingobject/AERT_Free
ms.topic: function
req.header: baseaudioprocessingobject.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating system,
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
req.lib: Audioeng.lib
req.dll: Audioeng.dll
req.irql: All levels
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Audioeng.dll
api_name:
 - AERT_Free
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AERT_Free function


## -description


The <code>AERT_Free</code> utility function releases (frees) memory that was locked by the <a href="https://msdn.microsoft.com/b992842d-0612-464c-9b82-b75137fa49eb">AERT_Allocate</a> function, for use by audio processing objects to process audio data.


## -parameters




### -param pMemory

A pointer to the memory that the <code>AERT_Free</code> function will free.


## -returns



The <code>AERT_Free</code> function returns a value of S_OK after it frees the locked memory.




## -remarks



None




## -see-also




<a href="https://msdn.microsoft.com/b992842d-0612-464c-9b82-b75137fa49eb">AERT_Allocate</a>
 

 

