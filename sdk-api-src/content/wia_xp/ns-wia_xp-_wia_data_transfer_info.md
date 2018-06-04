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

# _WIA_DATA_TRANSFER_INFO structure


## -description


The <b>WIA_DATA_TRANSFER_INFO</b> structure is used by applications to describe the buffer used to retrieve bands of data from Windows Image Acquisition (WIA) devices. It is primarily used in conjunction with the methods of the <a href="https://msdn.microsoft.com/565e48b7-30c5-4c8b-ae4a-071c2e90b2f9">IWiaDataTransfer</a> interface.


## -struct-fields




### -field ulSize

Type: <b>ULONG</b>

Contains the size of this structure. Must be set to <b>sizeof(WIA_DATA_TRANSFER_INFO)</b> before your application passes this structure to any WIA interface methods.


### -field ulSection

Type: <b>ULONG</b>

Specifies an optional handle to a shared section of memory allocated by the application. If this member is set to <b>NULL</b>, <a href="https://msdn.microsoft.com/3cbef4c0-cf28-4fdd-b347-84428ffd671b">IWiaDataTransfer::idtGetBandedData</a> allocates the shared memory itself.


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

