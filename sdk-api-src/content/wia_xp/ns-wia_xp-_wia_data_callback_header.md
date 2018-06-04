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

# _WIA_DATA_CALLBACK_HEADER structure


## -description


The <b>WIA_DATA_CALLBACK_HEADER</b> is transmitted to an application during a series of calls by the Windows Image Acquisition (WIA) run-time system to the <a href="https://msdn.microsoft.com/3f7fc88e-187e-41b1-a958-1f06ed81cb8f">IWiaDataCallback::BandedDataCallback</a> method.


## -struct-fields




### -field lSize

Type: <b>LONG</b>

Must contain the size of this structure in bytes. Should be initialized to <b>sizeof(WIA_DATA_CALLBACK_HEADER)</b>.


### -field guidFormatID

Type: <b>GUID</b>

Indicates the image clipboard format. For a list of clipboard formats, see <a href="winui._win32_SetClipboardData">SetClipboardData</a> Function. This parameter is queried during a callback to the <a href="https://msdn.microsoft.com/3f7fc88e-187e-41b1-a958-1f06ed81cb8f">IWiaDataCallback::BandedDataCallback</a> method with the <i>lMessage</i> parameter set to IT_MSG_DATA_HEADER.


### -field lBufferSize

Type: <b>LONG</b>

Specifies the size in bytes of the buffer needed for a complete data transfer. This value can be zero, which indicates that the total image size is unknown. (when using compressed data formats, for example). In this case, the application should dynamically increase the size of its buffer. For more information, see <a href="https://msdn.microsoft.com/ef48313e-4df4-4ccd-a085-f714100885a7">Common WIA Item Property Constants</a> in WIA_IPA_ITEM_SIZE.


### -field lPageCount

Type: <b>LONG</b>

Specifies the page count. Indicates the number of callbacks to the <a href="https://msdn.microsoft.com/3f7fc88e-187e-41b1-a958-1f06ed81cb8f">IWiaDataCallback::BandedDataCallback</a> method with the <i>lMessage</i>  parameter set to IT_MSG_NEW_PAGE.

