---
UID: NS:wia_xp._WIA_DATA_CALLBACK_HEADER
title: "_WIA_DATA_CALLBACK_HEADER"
author: windows-driver-content
description: The WIA_DATA_CALLBACK_HEADER is transmitted to an application during a series of calls by the Windows Image Acquisition (WIA) run-time system to the IWiaDataCallback::BandedDataCallback method.
old-location: wia\_wia_WIA_DATA_CALLBACK_HEADER.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\structs\wia_data_callback_header.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: "*PWIA_DATA_CALLBACK_HEADER, PWIA_DATA_CALLBACK_HEADER, PWIA_DATA_CALLBACK_HEADER structure pointer [WIA], WIA_DATA_CALLBACK_HEADER, WIA_DATA_CALLBACK_HEADER structure [WIA], _WIA_DATA_CALLBACK_HEADER, _wia_WIA_DATA_CALLBACK_HEADER, wia._wia_WIA_DATA_CALLBACK_HEADER, wia_xp/PWIA_DATA_CALLBACK_HEADER, wia_xp/WIA_DATA_CALLBACK_HEADER"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WIA_DATA_CALLBACK_HEADER, *PWIA_DATA_CALLBACK_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wia_xp.h
api_name:
-	WIA_DATA_CALLBACK_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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

