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

# IWICMetadataQueryReader::GetLocation


## -description


Retrieves the current path relative to the root metadata block.


## -parameters




### -param cchMaxLength [in]

Type: <b>UINT</b>

The length of the <i>wzNamespace</i> buffer.


### -param wzNamespace [in, out]

Type: <b>WCHAR*</b>

Pointer that receives the current namespace location.


### -param pcchActualLength [out]

Type: <b>UINT*</b>

The actual buffer length that was needed to retrieve the current namespace location.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If you pass <b>NULL</b> to <i>wzNamespace</i>, <b>GetLocation</b> ignores <i>cchMaxLength</i> and returns the required buffer length to store the path in the variable that <i>pcchActualLength</i> points to.


If the query reader is relative to the top of the metadata hierarchy, it will return a single-char string.

If the query reader is relative to a nested metadata block, this method will return the path to the current query reader.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/588e00d2-e166-4ce5-bd8a-50ad0d5a3db9">IWICMetadataQueryReader</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

