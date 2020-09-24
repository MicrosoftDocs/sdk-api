---
UID: NF:spatialaudioclient.IAudioFormatEnumerator.GetFormat
title: IAudioFormatEnumerator::GetFormat (spatialaudioclient.h)
description: Gets the format with the specified index in the list. The formats are listed in order of importance. The most preferable format is first in the list.
helpviewer_keywords: ["GetFormat","GetFormat method [Core Audio]","GetFormat method [Core Audio]","IAudioFormatEnumerator interface","IAudioFormatEnumerator interface [Core Audio]","GetFormat method","IAudioFormatEnumerator.GetFormat","IAudioFormatEnumerator::GetFormat","coreaudio.iaudioformatenumerator_getformat","spatialaudioclient/IAudioFormatEnumerator::GetFormat"]
old-location: coreaudio\iaudioformatenumerator_getformat.htm
tech.root: CoreAudio
ms.assetid: 9949F688-51D1-418B-947D-2607C90CA4E4
ms.date: 12/05/2018
ms.keywords: GetFormat, GetFormat method [Core Audio], GetFormat method [Core Audio],IAudioFormatEnumerator interface, IAudioFormatEnumerator interface [Core Audio],GetFormat method, IAudioFormatEnumerator.GetFormat, IAudioFormatEnumerator::GetFormat, coreaudio.iaudioformatenumerator_getformat, spatialaudioclient/IAudioFormatEnumerator::GetFormat
req.header: spatialaudioclient.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioFormatEnumerator::GetFormat
 - spatialaudioclient/IAudioFormatEnumerator::GetFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - IAudioFormatEnumerator.GetFormat
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

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-iaudioformatenumerator">IAudioFormatEnumerator</a>