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

# IWICFormatConverterInfo::GetPixelFormats


## -description


Retrieves a list of GUIDs that signify which pixel formats the converter supports.


## -parameters




### -param cFormats [in]

Type: <b>UINT</b>

The size of the <i>pPixelFormatGUIDs</i> array.


### -param pPixelFormatGUIDs [in, out]

Type: <b>WICPixelFormatGUID*</b>

Pointer to a GUID array that receives the pixel formats the converter supports.


### -param pcActual [out]

Type: <b>UINT*</b>

The actual array size needed to retrieve all pixel formats supported by the converter.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The format converter does not necessarily guarantee symmetricality with respect to conversion; that is, a converter may be able to convert FROM a particular format without actually being able to convert TO a particular format. In order to test symmetricality, use <a href="https://msdn.microsoft.com/bf813eaf-0899-4df2-bcc2-ba2db1e9af2f">CanConvert</a>.

To determine the number of pixel formats a coverter can handle, set <i>cFormats</i> to <code>0</code> and <i>pPixelFormatGUIDs</i> to <code>NULL</code>. The converter will fill <i>pcActual</i> with the number of formats supported by that converter.



