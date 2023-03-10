---
UID: NF:winddi.DrvDrawEscape
title: DrvDrawEscape function (winddi.h)
description: The DrvDrawEscape function is the entry point that serves more than one function call; the particular function depends on the value of the iEsc parameter.
helpviewer_keywords: ["DrvDrawEscape","DrvDrawEscape function [Display Devices]","ddifncs_d3db71f3-aafb-4718-a98f-4ef5d30a6b50.xml","display.drvdrawescape","winddi/DrvDrawEscape"]
old-location: display\drvdrawescape.htm
tech.root: display
ms.assetid: 698fb67e-4878-42ad-9c7a-899ddcbf1811
ms.date: 12/05/2018
ms.keywords: DrvDrawEscape, DrvDrawEscape function [Display Devices], ddifncs_d3db71f3-aafb-4718-a98f-4ef5d30a6b50.xml, display.drvdrawescape, winddi/DrvDrawEscape
req.header: winddi.h
req.include-header: Winddi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrvDrawEscape
 - winddi/DrvDrawEscape
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
 - DrvDrawEscape
---

# DrvDrawEscape function


## -description

The <b>DrvDrawEscape</b> function is the entry point that serves more than one function call; the particular function depends on the value of the <i>iEsc</i> parameter.

## -parameters

### -param pso [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that identifies the surface to which the call is directed.

### -param iEsc [in]

Specifies the operation to be performed. The meanings of the remaining parameters depend on this parameter. This parameter can be the following value. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
ESC_PASSTHROUGH

</td>
<td>
Passes raw device data to the device driver. The number of bytes of raw data is indicated by <i>cjIn</i>. The data is pointed to by <i>pvIn</i>. The return value is the number of bytes written if the function is successful. Otherwise, it is zero, and an error code is logged.

</td>
</tr>
</table>

### -param pco [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure that can be queried to find the area on the surface that the caller can overwrite.

### -param prcl [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure that defines the window rectangle on the surface. The application does not know the position of the window on the surface. GDI supplies this rectangle and holds a lock that ensures the rectangle is stable for the duration of the call. Coordinates received from the application are relative to the upper left corner of the window rectangle.

### -param cjIn [in]

Specifies the size, in bytes, of the buffer pointed to by <i>pvIn</i>.

### -param pvIn [in]

Pointer to the input data for the call. The format of the input data depends on the function specified by <i>iEsc</i>.

## -returns

The return value depends on the function specified by <i>iEsc</i>. The driver should return 0xFFFFFFFF if an unsupported function is called.

## -remarks

This entry point differs from <a href="/windows/desktop/api/winddi/nf-winddi-drvescape">DrvEscape</a> in that a CLIPOBJ structure is provided. This allows a driver to implement its own <a href="/windows-hardware/drivers/display/optional-display-driver-functions">drawing functions</a> in a windowed environment.

GDI passes data directly from a (possibly malicious) client application to the driver, which means that the <b>DrvDrawEscape</b> function must validate all input arguments. Specifically, this function must:

<ul>
<li>
Verify that the value received in the <i>iEsc</i> parameter represents a valid query.

</li>
<li>
Verify that the size of the input buffer (the value in the <i>cjIn</i> parameter) is valid for the specified query. 

</li>
<li>
Verify that the contents of the buffer pointed to by the <i>pvIn</i> parameter are valid for the specified query.

</li>
</ul>
The escapes that a device supports are determined by a call to <a href="/windows/desktop/api/winddi/nf-winddi-drvescape">DrvEscape</a>.

For more information about the escape codes that Microsoft reserves, see <a href="/windows/desktop/api/winddi/nf-winddi-drvescape">DrvEscape</a>.

<b>DrvDrawEscape</b> is optional for all drivers.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenabledriver">DrvEnableDriver</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvescape">DrvEscape</a>