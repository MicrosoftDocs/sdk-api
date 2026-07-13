---
UID: NS:wia_xp._WIA_DATA_TRANSFER_INFO
title: WIA_DATA_TRANSFER_INFO (wia_xp.h)
description: The WIA_DATA_TRANSFER_INFO structure is used by applications to describe the buffer used to retrieve bands of data from Windows Image Acquisition (WIA) devices. It is primarily used in conjunction with the methods of the IWiaDataTransfer interface.
helpviewer_keywords: ["*PWIA_DATA_TRANSFER_INFO","PWIA_DATA_TRANSFER_INFO","PWIA_DATA_TRANSFER_INFO structure pointer [WIA]","WIA_DATA_TRANSFER_INFO","WIA_DATA_TRANSFER_INFO structure [WIA]","_wia_WIA_DATA_TRANSFER_INFO","wia._wia_WIA_DATA_TRANSFER_INFO","wia_xp/PWIA_DATA_TRANSFER_INFO","wia_xp/WIA_DATA_TRANSFER_INFO"]
old-location: wia\_wia_WIA_DATA_TRANSFER_INFO.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\structs\wia_data_transfer_info.htm
ms.date: 12/05/2018
ms.keywords: '*PWIA_DATA_TRANSFER_INFO, PWIA_DATA_TRANSFER_INFO, PWIA_DATA_TRANSFER_INFO structure pointer [WIA], WIA_DATA_TRANSFER_INFO, WIA_DATA_TRANSFER_INFO structure [WIA], _wia_WIA_DATA_TRANSFER_INFO, wia._wia_WIA_DATA_TRANSFER_INFO, wia_xp/PWIA_DATA_TRANSFER_INFO, wia_xp/WIA_DATA_TRANSFER_INFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WIA_DATA_TRANSFER_INFO, *PWIA_DATA_TRANSFER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WIA_DATA_TRANSFER_INFO
 - wia_xp/_WIA_DATA_TRANSFER_INFO
 - PWIA_DATA_TRANSFER_INFO
 - wia_xp/PWIA_DATA_TRANSFER_INFO
 - WIA_DATA_TRANSFER_INFO
 - wia_xp/WIA_DATA_TRANSFER_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wia_xp.h
api_name:
 - WIA_DATA_TRANSFER_INFO
archived: true
---

# WIA_DATA_TRANSFER_INFO structure


## -description

The <b>WIA_DATA_TRANSFER_INFO</b> structure is used by applications to describe the buffer used to retrieve bands of data from Windows Image Acquisition (WIA) devices. It is primarily used in conjunction with the methods of the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer">IWiaDataTransfer</a> interface.

## -struct-fields

### -field ulSize

Type: <b>ULONG</b>

Contains the size of this structure. Must be set to <b>sizeof(WIA_DATA_TRANSFER_INFO)</b> before your application passes this structure to any WIA interface methods.

### -field ulSection

Type: <b>ULONG</b>

Specifies an optional handle to a shared section of memory allocated by the application. If this member is set to <b>NULL</b>, <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetbandeddata">IWiaDataTransfer::idtGetBandedData</a> allocates the shared memory itself.

### -field ulBufferSize

Type: <b>ULONG</b>

The size in bytes of the buffer that is used for the data transfer.

### -field bDoubleBuffer

Type: <b>BOOL</b>

Contains <b>TRUE</b> if the device is double buffered, <b>FALSE</b> if the device is not double buffered.

### -field ulReserved1

Type: <b>ULONG</b>

Reserved for use by the WIA system DLLs. Must be set to zero.

### -field ulReserved2

Type: <b>ULONG</b>

Reserved for use by the WIA system DLLs. Must be set to zero.

### -field ulReserved3

Type: <b>ULONG</b>

Reserved for use by the WIA system DLLs. Must be set to zero.