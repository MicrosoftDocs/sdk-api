---
UID: NI:winbio_ioctl.IOCTL_BIOMETRIC_GET_INDICATOR
title: IOCTL_BIOMETRIC_GET_INDICATOR
author: windows-driver-content
description: The IOCTL_BIOMETRIC_GET_INDICATOR IOCTL directs the driver to retrieve the status of the indicator light. This IOCTL is optional.
old-location: biometric\ioctl_biometric_get_indicator.htm
old-project: biometric
ms.assetid: 2fc5edbd-e042-41d0-84a2-9b6796b6e234
ms.author: windowsdriverdev
ms.date: 2/20/2018
ms.keywords: IOCTL_BIOMETRIC_GET_INDICATOR, IOCTL_BIOMETRIC_GET_INDICATOR control code [Biometric Devices], biometric.ioctl_biometric_get_indicator, biometric_ref_f257d48e-b4ad-4721-b780-10d3d98fa711.xml, winbio_ioctl/IOCTL_BIOMETRIC_GET_INDICATOR
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
-	IOCTL_BIOMETRIC_GET_INDICATOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IOCTL_BIOMETRIC_GET_INDICATOR IOCTL


## -description


The IOCTL_BIOMETRIC_GET_INDICATOR IOCTL directs the driver to retrieve the status of the indicator light.  This IOCTL is optional.


## -ioctlparameters




### -input-buffer

None.


### -input-buffer-length

None.


### -output-buffer

The AssociatedIrp.SystemBuffer member points to a buffer that contains a <a href="https://msdn.microsoft.com/library/windows/hardware/ff536471">WINBIO_GET_INDICATOR</a> structure.


### -output-buffer-length

The smallest valid output buffer size is the size of DWORD.  If the driver receives an DWORD-sized output buffer, the driver should return the buffer size necessary for the requested operation.


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



If the vendor-supplied driver passes back the entire payload, it should fill in the WinBioHresult member of WINBIO_GET_INDICATOR with the status of the biometric operation.

Possible values include:





