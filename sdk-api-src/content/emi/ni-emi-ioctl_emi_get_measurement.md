---
UID: NI:emi.IOCTL_EMI_GET_MEASUREMENT
title: IOCTL_EMI_GET_MEASUREMENT (emi.h)
description: The IOCTL_EMI_GET_MEASUREMENT control code retrieves the current energy measurement and the time at which the measurement was taken.
helpviewer_keywords: ["IOCTL_EMI_GET_MEASUREMENT","IOCTL_EMI_GET_MEASUREMENT control","IOCTL_EMI_GET_MEASUREMENT control code [Power Metering and Budgeting Devices]","emi/IOCTL_EMI_GET_MEASUREMENT","powermeter.ioctl_emi_get_measurement"]
old-location: powermeter\ioctl_emi_get_measurement.htm
tech.root: powermeter
ms.assetid: E23B1ED2-A87D-419A-8BEB-136AA77258AE
ms.date: 11/19/2021
ms.keywords: IOCTL_EMI_GET_MEASUREMENT, IOCTL_EMI_GET_MEASUREMENT control, IOCTL_EMI_GET_MEASUREMENT control code [Power Metering and Budgeting Devices], emi/IOCTL_EMI_GET_MEASUREMENT, powermeter.ioctl_emi_get_measurement
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
 - IOCTL_EMI_GET_MEASUREMENT
 - emi/IOCTL_EMI_GET_MEASUREMENT
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
 - IOCTL_EMI_GET_MEASUREMENT
---

# IOCTL_EMI_GET_MEASUREMENT IOCTL


## -description

The <b>IOCTL_EMI_GET_MEASUREMENT</b> 
   control code retrieves the current energy measurement and the time at which the measurement was taken.

## -ioctlparameters

### -input-buffer


<text> None. </text>

### -input-buffer-length

<text> None. </text>

### -output-buffer

<text> The  <b>AssociatedIrp.SystemBuffer</b> member specifies the address of a caller-allocated buffer that contains the measurement data from provider device driver. </text>

### -output-buffer-length

<text> The length of output buffer should be the size of [EMI_MEASUREMENT_DATA_V1](ns-emi-emi_channel_measurement_data.md) or [EMI_MEASUREMENT_DATA_V2](ns-emi-emi_measurement_data_v2.md) multiply by number of channels, it is specified in the <b> Parameters.DeviceIoControl.OutputBufferLength</b> member.  </text>


### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful. Otherwise, Status to the appropriate error condition as a NTSTATUS code. 


For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).


### -remarks
For EMI version 1 and 2, the EMI measurement data reported from each channel should be accumulated and translated to the unit specified by the channel on each request, as the EMI interface of any device should be shared across the system, therefore how freqeunt the counters are being sampled and accumulated depends on how often each of its consumer requests and also the driver implementation.


For the EMI version 2, Multiple channels are exposed by the same device should be sampled at once on each request, hence the caller should use the <b> ChannelCount </b> in the [EMI_METADATA_V2](ns-emi-emi_metadata_v2.md) to traverse the channels, for example:

```

  status = DeviceIoControl(DeviceHandle,
                           IOCTL_EMI_GET_MEASUREMENT,
                           NULL,
                           NULL,
                           Data,
                           ChannelDataSize,
                           BytesReturned,
                           NULL);

  EMI_CHANNEL_V2* Channel = &MetaData->Channels[0];
  for (int i = 0 ; i < MetaData->ChannelCount && status ; i++) {
      
      //
      // Get energy measurement for each energy counter.
      //

      AbsoluteEnergy = Measurement->ChannelData[i].AbsoluteEnergy;
      AbsoluteTime = Measurement->ChannelData[i].AbsoluteTime;
  }

```


## -see-also
[EMI_METADATA_V2](ns-emi-emi_metadata_v2.md) <br>
[EMI_MEASUREMENT_DATA_V2](ns-emi-emi_measurement_data_v2.md) <br>
<a href="/windows-hardware/drivers/powermeter/energy-meter-interface">Energy Metering Interface</a>