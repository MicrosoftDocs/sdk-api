---
UID: NI:winbio_ioctl.IOCTL_BIOMETRIC_CAPTURE_DATA
title: IOCTL_BIOMETRIC_CAPTURE_DATA
author: windows-driver-content
description: The IOCTL_BIOMETRIC_CAPTURE_DATA IOCTL directs the driver to retrieve the next scan of biometric data. This call should put the device into capture mode.Vendor-supplied WBDI drivers must support IOCTL_BIOMETRIC_CAPTURE_DATA.
old-location: biometric\ioctl_biometric_capture_data.htm
old-project: biometric
ms.assetid: 52c7007f-6038-41d8-b459-f0fa1b90fd5e
ms.author: windowsdriverdev
ms.date: 2/20/2018
ms.keywords: IOCTL_BIOMETRIC_CAPTURE_DATA, IOCTL_BIOMETRIC_CAPTURE_DATA control code [Biometric Devices], biometric.ioctl_biometric_capture_data, biometric_ref_8337ca76-e92a-4efe-a73f-3f23c01f35c2.xml, winbio_ioctl/IOCTL_BIOMETRIC_CAPTURE_DATA
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
-	IOCTL_BIOMETRIC_CAPTURE_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IOCTL_BIOMETRIC_CAPTURE_DATA IOCTL


## -description


The IOCTL_BIOMETRIC_CAPTURE_DATA IOCTL directs the driver to retrieve the next scan of biometric data.   This call should put the device into capture mode.Vendor-supplied WBDI drivers must support IOCTL_BIOMETRIC_CAPTURE_DATA.




## -ioctlparameters




### -input-buffer


<a href="https://msdn.microsoft.com/library/windows/hardware/ff536468">WINBIO_CAPTURE_PARAMETERS</a>



### -input-buffer-length

The length of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff536468">WINBIO_CAPTURE_PARAMETERS</a>
       structure.


### -output-buffer

The <b>AssociatedIrp</b>.<b>SystemBuffer</b> member points to a buffer that contains a <a href="https://msdn.microsoft.com/library/windows/hardware/ff536467">WINBIO_CAPTURE_DATA</a> structure.

The vendor-specific data in the WINBIO_BIR structure can be in any format the vendor would like to collect from the driver.  Vendors can choose to process data in the WBDI driver or in the engine adapter, but the data must be passed in one structure.  


### -output-buffer-length

The smallest valid output buffer size is the size of DWORD.

If the driver receives a DWORD-sized output buffer, the driver must immediately return the buffer size necessary to complete the operation.  Do not wait for the swipe to occur to send the required buffer size.


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
WINBIO_E_DATA_COLLECTION_IN_PROGRESS

</td>
<td>
Device has an IOCTL_BIOMETRIC_CAPTURE_DATA pending.

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



Only one data collection IOCTL can be pending at any time.  If the device has an IOCTL_BIOMETRIC_CAPTURE_DATA pending, IOCTL_BIOMETRIC_CAPTURE_DATA must return WINBIO_E_DATA_COLLECTION_IN_PROGRESS.

IOCTL_BIOMETRIC_CAPTURE_DATA is a blocking data collection IOCTL that is completed when the biometric data capture occurs. 

If the vendor-supplied driver passes back the entire payload, it should fill in the <b>WinBioHresult</b> member of WINBIO_CAPTURE_DATA with the status of the Biometric operation.

Possible values include:





