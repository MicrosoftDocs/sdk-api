---
UID: NF:winddi.DrvQueryDeviceSupport
title: DrvQueryDeviceSupport function
author: windows-sdk-content
description: The DrvQueryDeviceSupport function returns requested device-specific information.
old-location: display\drvquerydevicesupport.htm
old-project: display
ms.assetid: 684c5dd5-edf0-4b7d-888c-c01eb9670846
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DrvQueryDeviceSupport, DrvQueryDeviceSupport function [Display Devices], ddifncs_21186d04-cf17-4707-88b4-bd72d5f78b23.xml, display.drvquerydevicesupport, winddi/DrvQueryDeviceSupport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
req.target-type: Desktop
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvQueryDeviceSupport
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvQueryDeviceSupport function


## -description


The <b>DrvQueryDeviceSupport</b> function returns requested device-specific information.


## -parameters




### -param pso

Caller-supplied pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure.


### -param pxlo

Caller-supplied pointer to an <a href="https://msdn.microsoft.com/08bdead0-290a-4b23-8118-5f1f941e439f">XLATEOBJ</a> structure.


### -param pxo

Caller-supplied pointer to an <a href="https://msdn.microsoft.com/a18af8fc-880a-4ac3-905a-1d9384c2b8d7">XFORMOBJ</a> structure.


### -param iType

Caller-supplied bit flag indicating the type of information being requested. One of the following flags can be specified:

<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
QDS_CHECKJPEGFORMAT

</td>
<td>
The buffer pointed to by <i>pvIn</i> contains a JPEG-compressed image. The function must return <b>TRUE</b> if the device can print the image. Otherwise it must return <b>FALSE</b>.

</td>
</tr>
<tr>
<td>
QDS_CHECKPNGFORMAT

</td>
<td>
The buffer pointed to by <i>pvIn</i> contains a PNG-compressed image. The function must return <b>TRUE</b> if the device can print the image. Otherwise it must return <b>FALSE</b>.

</td>
</tr>
</table>
 


### -param cjIn

Caller-supplied size of the buffer pointed to by <i>pvIn</i>.


### -param pvIn [in]

Caller-supplied pointer to an input buffer.


### -param cjOut

Caller-supplied size of the buffer pointed to by <i>pvOut</i>.


### -param pvOut [out]

Caller-supplied pointer to an output buffer.


## -returns



If the operation succeeds, the function should return <b>TRUE</b>; otherwise it should return <b>FALSE</b>.




## -remarks



If the QDS_CHECKJPEGFORMAT or QDS_CHECKPNGFORMAT flag is set in <i>iType</i>, the following rules apply:

<ul>
<li>
The <i>pvIn</i> parameter points to a buffer containing a JPEG-compressed or PNG-compressed image. The driver must return <b>TRUE</b> if the image can be printed, or <b>FALSE</b> otherwise.

</li>
<li>
The <i>pxlo</i> parameter is valid but the only information of interest is the <a href="https://msdn.microsoft.com/08bdead0-290a-4b23-8118-5f1f941e439f">XLATEOBJ</a> structure's <b>flXlate</b> member. If either the XO_HOST_ICM or XO_DEVICE_ICM flag is set, the driver must only return <b>TRUE</b> if it can convert the image's color space to the printer's color space (or if the two color spaces are the same). For more information, see <a href="https://msdn.microsoft.com/ece0578d-bf03-4eee-9568-40ef684ba8a7">Color Management of JPEG and PNG Images</a>.

</li>
</ul>
For more information about supporting JPEG and PNG compressed images, see the Remarks section for <a href="https://msdn.microsoft.com/5ba3e521-2e70-4a5b-979d-30a061275d42">DEVINFO</a>.




## -see-also




<a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a>



<a href="https://msdn.microsoft.com/a18af8fc-880a-4ac3-905a-1d9384c2b8d7">XFORMOBJ</a>



<a href="https://msdn.microsoft.com/08bdead0-290a-4b23-8118-5f1f941e439f">XLATEOBJ</a>
 

 

