---
UID: NF:dwrite_3.IDWriteFontSet.GetPropertyOccurrenceCount
title: IDWriteFontSet::GetPropertyOccurrenceCount
author: windows-sdk-content
description: Returns how many times a given property value occurs in the set.
old-location: directwrite\idwritefontset_getpropertyoccurrencecount.htm
tech.root: DirectWrite
ms.assetid: 514359d4-595d-4cac-a784-527b65b53137
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetPropertyOccurrenceCount, GetPropertyOccurrenceCount method [Direct Write], GetPropertyOccurrenceCount method [Direct Write],IDWriteFontSet interface, IDWriteFontSet interface [Direct Write],GetPropertyOccurrenceCount method, IDWriteFontSet.GetPropertyOccurrenceCount, IDWriteFontSet::GetPropertyOccurrenceCount, directwrite.idwritefontset_getpropertyoccurrencecount, dwrite_3/IDWriteFontSet::GetPropertyOccurrenceCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontSet.GetPropertyOccurrenceCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite_3.h
: 
- IDWriteFontSet.GetPropertyOccurrenceCount
: 
---

# IDWriteFontSet::GetPropertyOccurrenceCount


## -description


Returns how many times a given property value occurs in the set.


## -parameters




### -param property [in]

Type: <b>const <a href="https://msdn.microsoft.com/C169B175-74FD-423A-8E0A-DC50314D75E6">DWRITE_FONT_PROPERTY</a>*</b>

Font property of interest.


### -param propertyOccurrenceCount [out]

Type: <b>UINT32*</b>

Receives how many times the property occurs.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0178f248-8dc0-c0ee-63c1-8db3f6ef94c3">IDWriteFontSet</a>
 

 

