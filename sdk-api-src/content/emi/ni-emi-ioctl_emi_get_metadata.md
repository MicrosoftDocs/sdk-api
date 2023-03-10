---
UID: NI:emi.IOCTL_EMI_GET_METADATA
title: IOCTL_EMI_GET_METADATA (emi.h)
description: The IOCTL_EMI_GET_METADATA control code retrieves EMI metadata from a device.
helpviewer_keywords: ["IOCTL_EMI_GET_METADATA","IOCTL_EMI_GET_METADATA control","IOCTL_EMI_GET_METADATA control code [Power Metering and Budgeting Devices]","emi/IOCTL_EMI_GET_METADATA","powermeter.ioctl_emi_get_metadata"]
old-location: powermeter\ioctl_emi_get_metadata.htm
tech.root: powermeter
ms.assetid: 3A1A76B0-2A46-4C15-84BC-CE75701C30B7
ms.date: 11/19/2021
ms.keywords: IOCTL_EMI_GET_METADATA, IOCTL_EMI_GET_METADATA control, IOCTL_EMI_GET_METADATA control code [Power Metering and Budgeting Devices], emi/IOCTL_EMI_GET_METADATA, powermeter.ioctl_emi_get_metadata
req.header: emi.h
req.include-header: Emi.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 10.
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
 - IOCTL_EMI_GET_METADATA
 - emi/IOCTL_EMI_GET_METADATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - emi.h
api_name:
 - IOCTL_EMI_GET_METADATA
---

# IOCTL_EMI_GET_METADATA IOCTL


## -description

The <b>IOCTL_EMI_GET_METADATA</b> 
   control code retrieves EMI metadata from a device. The metadata describe how EMI channels of the requesting device should be interpreted, and other related information.

## -ioctlparameters

### -input-buffer


<text> None. </text>

### -input-buffer-length

<text> None. </text>

### -output-buffer

<text> The <b> AssociatedIrp.SystemBuffer </b> 
    member specifies the address of a caller-allocated buffer that is used to retrieve the device-specific metadata that extended by [EMI_METADATA_V1](ns-emi-emi_metadata_v1.md) or [EMI_METADATA_V2](ns-emi-emi_metadata_v2.md) based on the interface version. On output, this structure holds the metadata of the channels of the requesting device. </text>

### -output-buffer-length

<text> The length of buffer should be either equal or greater than the value retrieved from [IOCTL_EMI_GET_METADATA_SIZE](ni-emi-ioctl_emi_get_metadata_size.md) and it is specified in the <b> Parameters.DeviceIoControl.OutputBufferLength </b> member.  </text>



### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).


### -remarks

In order to succesfully obtain the metadata, the caller should firstly obtain the version of metadata by [IOCTL_EMI_GET_VERSION](ni-emi-ioctl_emi_get_version.md) and secondly, the size of metadata by [IOCTL_EMI_GET_METADATA_SIZE](ni-emi-ioctl_emi_get_metadata_size.md)

One of the important information included in the metadata is the <b> Channels </b> , each channel represent an instance of a energy measurement counter that exposed by the device, caller should interpret the <b> Channels</b> dynamically according to the version.

For <b> EMI_VERSION_V1 </b>, the metadata describes a single channel by [EMI_METADATA_V1](ns-emi-emi_metadata_v1.md) structure.

For <b> EMI_VERSION_V2 </b>, the metadata describes multiple channels by [EMI_METADATA_V2](ns-emi-emi_metadata_v2.md) structure, which is a device-specific structure, therefore the size vary based on the driver implemenetation, the number of channels is specificed by <b> ChannelCount </b> in the metadata, which should be referenced to enumerate the <b> Channels </b> in the metadata. Also, the caller should use <b> EMI_CHANNEL_V2_NEXT_CHANNEL </b> to get each channel in a loop, this is because the size of each element in the <b> Channels </b> are also vary based on each <b> ChannelName </b>, for example:

```
    BOOL Status;
    EMI_METADATA_SIZE MetadataSize;
    EMI_METADATA_V2*  MetaData;

    ZeroMemory(&MetadataSize, sizeof(EMI_METADATA_SIZE));

    
    //  
    //  Retrieve the size of metadata.
    //

    Status = DeviceIoControl(DeviceHandle,
                             IOCTL_EMI_GET_METADATA_SIZE,
                             NULL,
                             NULL,
                             &MetadataSize,
                             sizeof(EMI_METADATA_SIZE),
                             BytesReturned,
                             NULL);

    if (!Status) {
        return Status;
    }

    //  
    //  Caller allocated buffer to retrieve the metadata.
    //

    
    MetaData = (EMI_METADATA_V2*)HeapAlloc(
                                    GetProcessHeap(),
                                    HEAP_ZERO_MEMORY,
                                    MetadataSize.MetadataSize);

    if (NULL == MetaData) {
        SetLastError(ERROR_OUTOFMEMORY);
        return FALSE;
    }

    
    //  
    //  Retrieve the metadata.
    //

    Status = DeviceIoControl(DeviceHandle,
                             IOCTL_EMI_GET_METADATA,
                             NULL,
                             NULL,
                             MetaData,
                             MetadataSize.MetadataSize,
                             BytesReturned,
                             NULL);

    //
    // Enumerate channels.
    //
    
    EMI_CHANNEL_V2* Channel = &MetaData->Channels[0];
    for (int i = 0 ; i < MetaData->ChannelCount ; i++) {
        
        //
        //  Get each EMI channel.
        //
        
        Channel = EMI_CHANNEL_V2_NEXT_CHANNEL(Channel);
    }

```

## -see-also

[EMI_METADATA_V2](ns-emi-emi_metadata_v2.md) <br>
<a href="/windows-hardware/drivers/powermeter/energy-meter-interface">Energy Metering Interface</a>