---
UID: NS:setupapi._SP_DRVINFO_DETAIL_DATA_W
title: SP_DRVINFO_DETAIL_DATA_W (setupapi.h)
description: An SP_DRVINFO_DETAIL_DATA structure contains detailed information about a particular driver information structure. (Unicode)
helpviewer_keywords: ["*PSP_DRVINFO_DETAIL_DATA_W","PSP_DRVINFO_DETAIL_DATA","PSP_DRVINFO_DETAIL_DATA structure pointer [Device and Driver Installation]","SP_DRVINFO_DETAIL_DATA","SP_DRVINFO_DETAIL_DATA structure [Device and Driver Installation]","SP_DRVINFO_DETAIL_DATA_W","devinst.sp_drvinfo_detail_data","di-struct_74ef2af7-e982-4041-9c39-605ca316359c.xml","setupapi/PSP_DRVINFO_DETAIL_DATA","setupapi/SP_DRVINFO_DETAIL_DATA"]
old-location: devinst\sp_drvinfo_detail_data.htm
tech.root: devinst
ms.assetid: 6e16a90a-a876-471c-917b-a26229a9187a
ms.date: 12/05/2018
ms.keywords: '*PSP_DRVINFO_DETAIL_DATA_W, PSP_DRVINFO_DETAIL_DATA, PSP_DRVINFO_DETAIL_DATA structure pointer [Device and Driver Installation], SP_DRVINFO_DETAIL_DATA, SP_DRVINFO_DETAIL_DATA structure [Device and Driver Installation], SP_DRVINFO_DETAIL_DATA_W, devinst.sp_drvinfo_detail_data, di-struct_74ef2af7-e982-4041-9c39-605ca316359c.xml, setupapi/PSP_DRVINFO_DETAIL_DATA, setupapi/SP_DRVINFO_DETAIL_DATA'
req.header: setupapi.h
req.include-header: Setupapi.h
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
req.typenames: SP_DRVINFO_DETAIL_DATA_W, *PSP_DRVINFO_DETAIL_DATA_W
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_DRVINFO_DETAIL_DATA_W
 - setupapi/_SP_DRVINFO_DETAIL_DATA_W
 - PSP_DRVINFO_DETAIL_DATA_W
 - setupapi/PSP_DRVINFO_DETAIL_DATA_W
 - SP_DRVINFO_DETAIL_DATA_W
 - setupapi/SP_DRVINFO_DETAIL_DATA_W
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - setupapi.h
api_name:
 - SP_DRVINFO_DETAIL_DATA
 - sp_drvinfo_detail_data_w
---

# SP_DRVINFO_DETAIL_DATA_W structure


## -description

An SP_DRVINFO_DETAIL_DATA structure contains detailed information about a particular driver information structure.

## -struct-fields

### -field cbSize

The size, in bytes, of the SP_DRVINFO_DETAIL_DATA structure.

### -field InfDate

Date of the INF file for this driver.

### -field CompatIDsOffset

The offset, in characters, from the beginning of the <b>HardwareID</b> buffer where the CompatIDs list begins.

This value can also be used to determine whether there is a <a href="/windows-hardware/drivers/install/hardware-ids">hardware ID</a> that precedes the CompatIDs list. If this value is greater than 1, the first string in the <b>HardwareID</b> buffer is the hardware ID. If this value is less than or equal to 1, there is no hardware ID.

### -field CompatIDsLength

The length, in characters, of the CompatIDs list starting at offset <b>CompatIDsOffset</b> from the beginning of the <b>HardwareID</b> buffer. 

If <b>CompatIDsLength</b> is nonzero, the CompatIDs list contains one or more NULL-terminated strings with an additional NULL character at the end of the list.

If <b>CompatIDsLength</b> is zero, the CompatIDs list is empty. In that case, there is no additional NULL character at the end of the list.

### -field Reserved

Reserved. For internal use only.

### -field SectionName

A NULL-terminated string that contains the name of the <a href="/windows-hardware/drivers/install/inf-ddinstall-section">INF DDInstall section</a> for this driver. This must be the basic <i>DDInstall</i> section name, such as <b>InstallSec</b>, without any OS/architecture-specific extensions.

### -field InfFileName

A NULL-terminated string that contains the full-qualified name of the INF file for this driver.

### -field DrvDescription

A NULL-terminated string that describes the driver.

### -field HardwareID

A buffer that contains a list of IDs (a single <a href="/windows-hardware/drivers/install/hardware-ids">hardware ID</a> followed by a list of <a href="/windows-hardware/drivers/install/compatible-ids">compatible IDs</a>). These IDs correspond to the hardware ID and compatible IDs in the <a href="/windows-hardware/drivers/install/inf-models-section">INF Models section</a>. 

Each ID in the list is a NULL-terminated string.

If the hardware ID exists (that is, if <b>CompatIDsOffset</b> is greater than one), this single NULL-terminated string is found at the beginning of the buffer. 

If the CompatIDs list is not empty (that is, if <b>CompatIDsLength</b> is not zero), the CompatIDs list starts at offset <b>CompatIDsOffset</b> from the beginning of this buffer, and is terminated with an additional NULL character at the end of the list.

## -remarks

The <a href="/windows-hardware/drivers/install/hardware-ids">hardware ID</a> and <a href="/windows-hardware/drivers/install/compatible-ids">compatible IDs</a> for a device are specified in the <a href="/windows-hardware/drivers/install/inf-models-section">INF Models section</a> in the following order:

<ul>
<li>
The first ID (if specified) is the hardware ID for the device.

</li>
<li>
The remaining IDs (if specified) are compatible IDs for the device.

</li>
</ul>
When you parse the <b>HardwareID</b> buffer, you must ensure that you correctly determine the end of the data in the buffer. Be aware that the buffer is not necessarily double NULL terminated.

For example, depending on how the list of <a href="/windows-hardware/drivers/install/hardware-ids">hardware ID</a> and <a href="/windows-hardware/drivers/install/compatible-ids">compatible IDs</a> are specified in the <a href="/windows-hardware/drivers/install/inf-models-section">INF Models section</a>, the <b>HardwareID</b> buffer can resemble any of the following:

<ul>
<li>
\0

</li>
<li>
&lt;HWID&gt;\0

</li>
<li>
&lt;HWID&gt;\0&lt;COMPATID_1&gt;\0...&lt;COMPATID_N&gt;\0\0

</li>
<li>
\0&lt;COMPATID_1&gt;\0...&lt;COMPATID_N&gt;\0\0

</li>
</ul>
An algorithm to correctly parse this buffer must use the <b>CompatIDsOffset</b> and <b>CompatIDsLength</b> fields to extract the <a href="/windows-hardware/drivers/install/hardware-ids">hardware ID</a> and <a href="/windows-hardware/drivers/install/compatible-ids">compatible IDs</a>, as shown in the following code example:


```
// parse the hardware ID, if it exists
if (CompatIDsOffset > 1)
{
    // Parse for hardware ID from index 0. 
    // This is a single NULL-terminated string
}
 // Parse the compatible IDs, if they exist
if (CompatIDsLength > 0)
{
    // Parse for list of compatible IDs from CompatIDsOffset. 
    // This is a double NULL-terminated list of strings (i.e. MULTI-SZ)
}
```






> [!NOTE]
> The setupapi.h header defines SP_DRVINFO_DETAIL_DATA as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows-hardware/drivers/install/compatible-ids">Compatible IDs</a>



<a href="/windows-hardware/drivers/install/hardware-ids">Hardware ID</a>



<a href="/windows-hardware/drivers/install/inf-ddinstall-section">INF DDInstall Section</a>



<a href="/windows-hardware/drivers/install/inf-models-section">INF Models Section</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdriverinfodetaila">SetupDiGetDriverInfoDetail</a>
