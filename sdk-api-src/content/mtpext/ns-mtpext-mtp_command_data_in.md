---
UID: NS:mtpext._MTP_COMMAND_DATA_IN
title: MTP_COMMAND_DATA_IN (mtpext.h)
description: The MTP_COMMAND_DATA_IN structure contains Media Transport Protocol (MTP) custom commands that are sent to the device by using the IWMDMDevice3::DeviceIoControl method.
helpviewer_keywords: ["*PMTP_COMMAND_DATA_IN","MTP_COMMAND_DATA_IN","MTP_COMMAND_DATA_IN structure [windows Media Device Manager]","PMTP_COMMAND_DATA_IN","PMTP_COMMAND_DATA_IN structure pointer [windows Media Device Manager]","mtpext/MTP_COMMAND_DATA_IN","mtpext/PMTP_COMMAND_DATA_IN","wmdm.mtp_command_data_in"]
old-location: wmdm\mtp_command_data_in.htm
tech.root: WMDM
ms.assetid: a7a6871b-3d53-4134-9877-398c532b489f
ms.date: 12/05/2018
ms.keywords: '*PMTP_COMMAND_DATA_IN, MTP_COMMAND_DATA_IN, MTP_COMMAND_DATA_IN structure [windows Media Device Manager], PMTP_COMMAND_DATA_IN, PMTP_COMMAND_DATA_IN structure pointer [windows Media Device Manager], mtpext/MTP_COMMAND_DATA_IN, mtpext/PMTP_COMMAND_DATA_IN, wmdm.mtp_command_data_in'
req.header: mtpext.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MTP_COMMAND_DATA_IN, *PMTP_COMMAND_DATA_IN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MTP_COMMAND_DATA_IN
 - mtpext/_MTP_COMMAND_DATA_IN
 - PMTP_COMMAND_DATA_IN
 - mtpext/PMTP_COMMAND_DATA_IN
 - MTP_COMMAND_DATA_IN
 - mtpext/MTP_COMMAND_DATA_IN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MtpExt.h
api_name:
 - MTP_COMMAND_DATA_IN
---

## -description

The <b>MTP_COMMAND_DATA_IN</b> structure contains Media Transport Protocol (MTP) custom commands that are sent to the device by using the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol">IWMDMDevice3::DeviceIoControl</a> method.

## -struct-fields

### -field OpCode

Operation code.

### -field NumParams

Number of parameters passed in.

### -field Params

Parameters to the command. <b>MTP_COMMAND_MAX_PARAMS</b> is a defined constant with a value of 5.

### -field NextPhase

Indicates whether the command has a read data phase, a write data phase, or no data phase. The valid values are defined in the following table.

### -field CommandWriteDataSize

Data size of <b>CommandWriteData</b>[1], in bytes.

### -field CommandWriteData

Optional, first byte of data to write to the device if <b>NextPhase</b> is MTP_NEXTPHASE_WRITE_DATA.

## -remarks

The input buffer is expected to contain an appropriately filled out <b>MTP_COMMAND_DATA_IN</b> structure. On exit, the device driver will fill out the <b>MTP_COMMAND_DATA_OUT</b> structure and save it to the output buffer. Therefore, any request must have an input buffer of at least SIZEOF_REQUIRED_COMMAND_DATA_IN bytes, which is defined as

``` syntax
#define SIZEOF_REQUIRED_COMMAND_DATA_IN (sizeof(MTP_COMMAND_DATA_IN)-1)
```

and an output buffer of at least SIZEOF_REQUIRED_COMMAND_DATA_OUT bytes, which is defined as

``` syntax
#define SIZEOF_REQUIRED_COMMAND_DATA_OUT (sizeof(MTP_COMMAND_DATA_OUT)-1)
```

It is assumed that all commands are self-contained, that is, they can be processed completely in one call. This has implications on lengthy data transfers, because chunking in the traditional sense is not supported. (For example, to issue a read for 3megabytes, the caller would have to ensure that it allocates an output buffer of 3 MB plus SIZEOF_REQUIRED_COMMAND_DATA_OUT bytes.) Lengthy data transfers should not be done with this method, but rather through normal data-transfer APIs.

## -see-also

* <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol">IWMDMDevice3::DeviceIoControl</a>
* <a href="/windows/win32/api/mtpext/ns-mtpext-mtp_command_data_out">MTP_COMMAND_DATA_OUT</a>
* <a href="/windows/desktop/WMDM/structures">Structures</a>
