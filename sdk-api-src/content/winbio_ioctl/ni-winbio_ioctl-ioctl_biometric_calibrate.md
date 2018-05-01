---
UID: NI:winbio_ioctl.IOCTL_BIOMETRIC_CALIBRATE
title: IOCTL_BIOMETRIC_CALIBRATE
author: windows-driver-content
description: The IOCTL_BIOMETRIC_CALIBRATE IOCTL directs the driver to perform any necessary steps to calibrate the device for use.
old-location: biometric\ioctl_biometric_calibrate.htm
old-project: biometric
ms.assetid: 3ffd954f-91f8-4896-b105-86e07a5b6be7
ms.author: windowsdriverdev
ms.date: 2/20/2018
ms.keywords: IOCTL_BIOMETRIC_CALIBRATE, IOCTL_BIOMETRIC_CALIBRATE control code [Biometric Devices], biometric.ioctl_biometric_calibrate, biometric_ref_160131c1-3389-4869-89c5-0d01761930e2.xml, winbio_ioctl/IOCTL_BIOMETRIC_CALIBRATE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: winbio_ioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 and later versions of Windows.
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
req.typenames: WINBIO_STORAGE_RECORD, *PWINBIO_STORAGE_RECORD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winbio_ioctl.h
api_name:
-	IOCTL_BIOMETRIC_CALIBRATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IOCTL_BIOMETRIC_CALIBRATE IOCTL


## -description


The IOCTL_BIOMETRIC_CALIBRATE IOCTL directs the driver to perform any necessary steps to calibrate the device for use.  Internally, the driver may also collect and return vendor specific calibration data to be analyzed by an application. Vendor-supplied WBDI drivers must support this IOCTL.


## -ioctlparameters




### -input-buffer

None.


### -input-buffer-length

None.


### -output-buffer

The <b>AssociatedIrp</b>.<b>SystemBuffer</b> member points to a buffer that contains a <a href="https://msdn.microsoft.com/library/windows/hardware/ff536465">WINBIO_CALIBRATION_INFO</a> structure.


### -output-buffer-length

Length of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff536465">WINBIO_CALIBRATION_INFO</a> structure. 

The vendor-supplied driver can optionally return a DWORD-sized buffer that specifies the buffer size necessary for the requested operation.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

Indicates whether the DeviceIoControl call to the driver completed and the OUT payload is valid.

The <b>Status</b> member is set to one of the values in the following table.

<table>
<tr>
<th>Status value</th>
<th>Description</th>
</tr>
<tr>
<td>
S_OK, STATUS_SUCCESS

</td>
<td>
The operation completed successfully.  If the size of data returned is DWORD, the payload contains the size of the buffer necessary for the call.  Otherwise, the payload contains the full output buffer.

</td>
</tr>
<tr>
<td>
E_INVALIDARG

</td>
<td>
The parameters were not specified correctly.

</td>
</tr>
<tr>
<td>
E_UNKNOWN

</td>
<td>
Any other failure that prevents the payload from being filled in.

</td>
</tr>
<tr>
<td>
E_UNEXPECTED

</td>
<td>
Any other failure that prevents the payload from being filled in.

</td>
</tr>
<tr>
<td>
E_FAIL

</td>
<td>
Any other failure that prevents the payload from being filled in.

</td>
</tr>
</table>
 


## -remarks



If the vendor-supplied driver passes back the entire payload, it should fill in the <b>WinBioHresult</b> member of WINBIO_CALIBRATION_INFO with the status of the Biometric operation.



