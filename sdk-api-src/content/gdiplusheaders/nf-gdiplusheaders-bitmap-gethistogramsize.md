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

# Bitmap::GetHistogramSize


## -description


The <b>Bitmap::GetHistogramSize</b> returns the number of elements (in an array of <b>UINT</b>s) that you must allocate before you call the <a href="https://msdn.microsoft.com/c7dcc384-54b1-457a-86cd-e27b232a9152">Bitmap::GetHistogram</a> method of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a> object.


## -parameters




### -param format [in]

Type: <b><a href="https://msdn.microsoft.com/1769ec16-e915-4a87-83d4-0989a4d79e85">HistogramFormat</a></b>

Element of the <a href="https://msdn.microsoft.com/1769ec16-e915-4a87-83d4-0989a4d79e85">HistogramFormat</a> enumeration that specifies the pixel format of the bitmap.


### -param NumberOfEntries [out]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that receives the number of entries.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>
 

 

