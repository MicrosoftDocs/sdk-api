---
UID: NF:spatialaudioclient.IAudioFormatEnumerator.GetFormat
title: IAudioFormatEnumerator::GetFormat
author: windows-sdk-content
description: Gets the format with the specified index in the list. The formats are listed in order of importance. The most preferable format is first in the list.
old-location: coreaudio\iaudioformatenumerator_getformat.htm
old-project: CoreAudio
ms.assetid: 9949F688-51D1-418B-947D-2607C90CA4E4
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetFormat, GetFormat method [Core Audio], GetFormat method [Core Audio],IAudioFormatEnumerator interface, IAudioFormatEnumerator interface [Core Audio],GetFormat method, IAudioFormatEnumerator.GetFormat, IAudioFormatEnumerator::GetFormat, coreaudio.iaudioformatenumerator_getformat, spatialaudioclient/IAudioFormatEnumerator::GetFormat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: spatialaudioclient.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AudioObjectType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - IAudioFormatEnumerator.GetFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IAudioFormatEnumerator::GetFormat


## -description


Gets the format with the specified index in the list. The formats are listed in order of importance. The most preferable format is first in the list.


## -parameters




### -param index [in]

The index of the item in the list to retrieve.


### -param format [out]

Pointer to a pointer to a <b>WAVEFORMATEX</b> structure describing a supported audio format.


## -returns



If the method succeeds, it returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/50434617-E70E-4931-B98E-61650E9DEA7E">IAudioFormatEnumerator</a>
 

 

