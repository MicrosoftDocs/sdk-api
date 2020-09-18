---
UID: NS:winddi.tagDRVENABLEDATA
title: DRVENABLEDATA (winddi.h)
description: The DRVENABLEDATA structure contains a pointer to an array of DRVFN structures and the graphics DDI version number of an NT-based operating system.
helpviewer_keywords: ["*PDRVENABLEDATA","DRVENABLEDATA","DRVENABLEDATA structure [Display Devices]","PDRVENABLEDATA","PDRVENABLEDATA structure pointer [Display Devices]","display.drvenabledata","grstrcts_d39f1feb-36e3-4fc6-b580-5b428dbeebd0.xml","winddi/DRVENABLEDATA","winddi/PDRVENABLEDATA"]
old-location: display\drvenabledata.htm
tech.root: display
ms.assetid: dbeaecf8-dea1-4412-babb-6e40bf5dc7b0
ms.date: 12/05/2018
ms.keywords: '*PDRVENABLEDATA, DRVENABLEDATA, DRVENABLEDATA structure [Display Devices], PDRVENABLEDATA, PDRVENABLEDATA structure pointer [Display Devices], display.drvenabledata, grstrcts_d39f1feb-36e3-4fc6-b580-5b428dbeebd0.xml, winddi/DRVENABLEDATA, winddi/PDRVENABLEDATA'
req.header: winddi.h
req.include-header: Winddi.h
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
req.typenames: DRVENABLEDATA, *PDRVENABLEDATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDRVENABLEDATA
 - winddi/tagDRVENABLEDATA
 - PDRVENABLEDATA
 - winddi/PDRVENABLEDATA
 - DRVENABLEDATA
 - winddi/DRVENABLEDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DRVENABLEDATA
---

# DRVENABLEDATA structure


## -description

The DRVENABLEDATA structure contains a pointer to an array of <a href="/windows/desktop/api/winddi/ns-winddi-drvfn">DRVFN</a> structures and the graphics DDI version number of an NT-based operating system.

## -struct-fields

### -field iDriverVersion

Specifies the graphics DDI version number of the NT-based operating system that the driver is targeted for. This member can be set to one of the following values:

<table>
<tr>
<th>Value</th>
<th>Operating System Version</th>
</tr>
<tr>
<td>
DDI_DRIVER_VERSION_NT4

</td>
<td>
Windows NT 4.0

</td>
</tr>
<tr>
<td>
DDI_DRIVER_VERSION_SP3

</td>
<td>
Windows NT 4.0 Service Pack 3

</td>
</tr>
<tr>
<td>
DDI_DRIVER_VERSION_NT5

</td>
<td>
Windows 2000

</td>
</tr>
<tr>
<td>
DDI_DRIVER_VERSION_NT5_01

</td>
<td>
Windows XP

</td>
</tr>
<tr>
<td>
DDI_DRIVER_VERSION_NT5_01_SP1

</td>
<td>
Windows XP Service Pack 1

</td>
</tr>
</table>
 

See the Remarks section for more information.

### -field c

Specifies the number of <a href="/windows/desktop/api/winddi/ns-winddi-drvfn">DRVFN</a> structures in the buffer pointed to by the <b>pdrvfn</b> member.

### -field pdrvfn

Pointer to a buffer containing an array of <a href="/windows/desktop/api/winddi/ns-winddi-drvfn">DRVFN</a> structures.

## -remarks

To run on these NT-based operating systems versions, the <b>iDriverVersion</b> member must be set as follows:

<table>
<tr>
<th>Windows version</th>
<th>Value of iDriverVersion</th>
</tr>
<tr>
<td>
Windows NT 4.0

</td>
<td>
<b>iDriverVersion</b> == DDI_DRIVER_VERSION_NT4

</td>
</tr>
<tr>
<td>
Windows NT 4.0 SP3

</td>
<td>
DDI_DRIVER_VERSION_NT4 &lt;= <b>iDriverVersion</b> &lt;= DDI_DRIVER_VERSION_SP3

</td>
</tr>
<tr>
<td>
Windows 2000

</td>
<td>
DDI_DRIVER_VERSION_NT4 &lt;= <b>iDriverVersion</b> &lt;= DDI_DRIVER_VERSION_NT5

</td>
</tr>
<tr>
<td>
Windows XP

</td>
<td>
DDI_DRIVER_VERSION_NT4 &lt;= <b>iDriverVersion</b> &lt;= DDI_DRIVER_VERSION_NT5_01

</td>
</tr>
<tr>
<td>
Windows XP SP1

</td>
<td>
DDI_DRIVER_VERSION_NT4 &lt;= <b>iDriverVersion</b> &lt;= DDI_DRIVER_VERSION_NT5_01_SP1

</td>
</tr>
</table>
 

As the table shows, a driver can run on any of these operating system versions if <b>iDriverVersion</b> is set to DDI_DRIVER_VERSION_NT4, but a driver can run only on Windows XP and later versions of the operating system if <b>iDriverVersion</b> is set to DDI_DRIVER_VERSION_NT5_01.

<div class="alert"><b>Note</b>  If a driver implements a <i>DrvXxx</i> graphics DDI that is not supported in all versions of Windows, the driver cannot specify a DRVFN entry for that graphics DDI when running on versions of Windows that do not support it. If the driver does specify a DRVFN entry for such a graphics DDI, Windows will reject the driver. The <i>permedia2</i> sample demonstrates how to specify different DRVFN structures for different versions of Windows.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-drvfn">DRVFN</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenabledriver">DrvEnableDriver</a>