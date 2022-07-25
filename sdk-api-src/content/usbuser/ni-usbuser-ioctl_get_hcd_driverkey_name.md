---
UID: NI:usbuser.IOCTL_GET_HCD_DRIVERKEY_NAME
title: IOCTL_GET_HCD_DRIVERKEY_NAME (usbuser.h)
description: The IOCTL_GET_HCD_DRIVERKEY_NAME I/O control request retrieves the driver key name in the registry for a USB host controller driver.
old-location: buses\ioctl_get_hcd_driverkey_name.htm
tech.root: buses
ms.assetid: 2435ef20-c75c-4b28-9824-8428b2ac6326
ms.date: 12/05/2018
ms.keywords: IOCTL_GET_HCD_DRIVERKEY_NAME, IOCTL_GET_HCD_DRIVERKEY_NAME control, IOCTL_GET_HCD_DRIVERKEY_NAME control code [Buses], buses.ioctl_get_hcd_driverkey_name, usbirp_e5bfae17-3a5d-414d-a24d-6c09269618aa.xml, usbuser/IOCTL_GET_HCD_DRIVERKEY_NAME
req.header: usbuser.h
req.include-header: Usbioctl.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOCTL_GET_HCD_DRIVERKEY_NAME
 - usbuser/IOCTL_GET_HCD_DRIVERKEY_NAME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - usbuser.h
api_name:
 - IOCTL_GET_HCD_DRIVERKEY_NAME
---

# IOCTL_GET_HCD_DRIVERKEY_NAME IOCTL


## -description

The <b>IOCTL_GET_HCD_DRIVERKEY_NAME</b> I/O control request retrieves the driver key name in the registry for a USB host controller driver.



<b>IOCTL_GET_HCD_DRIVERKEY_NAME</b> is a user-mode I/O control request. This request targets the USB host controller (GUID_DEVINTERFACE_USB_HOST_CONTROLLER).

## -ioctlparameters

### -input-buffer

None.

### -input-buffer-length

None.

### -output-buffer

The <b>AssociatedIrp.SystemBuffer</b> member specifies the address of a caller-allocated buffer that contains a <a href="/windows-hardware/drivers/ddi/content/usbioctl/ns-usbioctl-_usb_hcd_driverkey_name">USB_HCD_DRIVERKEY_NAME</a> structure. On output, this structure holds the driver key name. For more information, see Remarks.

### -output-buffer-length

The size of this buffer is specified in the <b>Parameters.DeviceIoControl.OutputBufferLength</b> member.

### -in-out-buffer


### -inout-buffer-length


### -status-block

The USB stack sets <b>Irp-&gt;IoStatus.Status</b> to STATUS_SUCCESS if the request is successful. Otherwise, the USB stack sets <b>Status</b> to the appropriate error condition, such as STATUS_INVALID_PARAMETER or STATUS_INSUFFICIENT_RESOURCES.

## -remarks

To get the driver key name in  the registry, you must perform the following tasks: 

<ol>
<li>Declare a variable of the type <a href="/windows-hardware/drivers/ddi/content/usbioctl/ns-usbioctl-_usb_hcd_driverkey_name">USB_HCD_DRIVERKEY_NAME</a>.</li>
<li>Send an <b>IOCTL_GET_HCD_DRIVERKEY_NAME</b> request by specifying the address and size of the variable in the output parameters. On return, the <b>ActualLength</b> member of  <a href="/windows-hardware/drivers/ddi/content/usbioctl/ns-usbioctl-_usb_hcd_driverkey_name">USB_HCD_DRIVERKEY_NAME</a> contains the length required to allocate a buffer to hold a <b>USB_HCD_DRIVERKEY_NAME</b> that is populated with the driver key name.</li>
<li>Allocate memory for a buffer to hold a <a href="/windows-hardware/drivers/ddi/content/usbioctl/ns-usbioctl-_usb_hcd_driverkey_name">USB_HCD_DRIVERKEY_NAME</a> structure. The size of the buffer  must be  the received <b>ActualLength</b> value.</li>
<li>Send an <b>IOCTL_GET_HCD_DRIVERKEY_NAME</b> request by passing a pointer to the allocated buffer and its size in the output parameters. On return, the <b>DriverKeyName</b> member of  <a href="/windows-hardware/drivers/ddi/content/usbioctl/ns-usbioctl-_usb_hcd_driverkey_name">USB_HCD_DRIVERKEY_NAME</a> is a null-terminated Unicode string that contains the name of the driver key associated with the host controller driver. </li>
</ol>
The following example code shows how to send the <b>IOCTL_GET_HCD_DRIVERKEY_NAME</b> I/O control request.


```cpp

/*++

Routine Description:

This routine prints the name of the driver key associated with
the specified host controller driver.

Arguments:

HCD - Handle for host controller driver.

Return Value: Boolean that indicates success or failure.

--*/

BOOL GetHCDDriverKeyName (HANDLE  HCD)
{
    BOOL                    success;
    ULONG                   nBytes;
    USB_HCD_DRIVERKEY_NAME  driverKeyName;
    PUSB_HCD_DRIVERKEY_NAME driverKeyNameW;

    driverKeyNameW = NULL;

    // 1. Get the length of the name of the driver key.
    success = DeviceIoControl(HCD,
        IOCTL_GET_HCD_DRIVERKEY_NAME,
        NULL,
        0,
        &driverKeyName,
        sizeof(driverKeyName),
        &nBytes,
        NULL);

    if (!success) 
    {
        printf("First IOCTL_GET_HCD_DRIVERKEY_NAME request failed\n");
        goto GetHCDDriverKeyNameDone;
    }

    //2. Get the length of the driver key name.
    nBytes = driverKeyName.ActualLength;

    if (nBytes <= sizeof(driverKeyName)) 
    {
        printf("Incorrect length received by IOCTL_GET_HCD_DRIVERKEY_NAME.\n");
        goto GetHCDDriverKeyNameDone;
    }

    // 3. Allocate memory for a USB_HCD_DRIVERKEY_NAME
    //    to hold the driver key name.
    driverKeyNameW = (PUSB_HCD_DRIVERKEY_NAME) malloc(nBytes);

    if (driverKeyNameW == NULL) 
    {
        printf("Failed to allocate memory.\n");
        goto GetHCDDriverKeyNameDone;
    }

    // Get the name of the driver key of the device attached to
    // the specified port.
    success = DeviceIoControl(HCD,
        IOCTL_GET_HCD_DRIVERKEY_NAME,
        NULL,
        0,
        driverKeyNameW,
        nBytes,
        &nBytes,
        NULL);

    if (!success) 
    {
        printf("Second IOCTL_GET_HCD_DRIVERKEY_NAME request failed.\n");
        goto GetHCDDriverKeyNameDone;
    }

    // print the driver key name. 
    printf("Driver Key Name: %s.\n", driverKeyNameW->DriverKeyName);


GetHCDDriverKeyNameDone:

    // Cleanup.
    // Free the allocated memory for USB_HCD_DRIVERKEY_NAME.

    if (driverKeyNameW != NULL) 
    {
        free(driverKeyNameW);
        driverKeyNameW = NULL;
    }

    return success;
}


```

## -see-also

<a href="/windows-hardware/drivers/ddi/content/usbioctl/ns-usbioctl-_usb_hcd_driverkey_name">USB_HCD_DRIVERKEY_NAME</a>