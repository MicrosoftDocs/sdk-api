---
UID: NS:ddrawint._DD_GETDRIVERSTATEDATA
title: DD_GETDRIVERSTATEDATA (ddrawint.h)
description: The DD_GETDRIVERSTATEDATA structure describes the state of the driver.
helpviewer_keywords: ["*PDD_GETDRIVERSTATEDATA","DD_GETDRIVERSTATEDATA","DD_GETDRIVERSTATEDATA structure [Display Devices]","d3dstrct_a7ee9601-b71c-4ff4-8ac5-37b62608d463.xml","ddrawint/DD_GETDRIVERSTATEDATA","display.dd_getdriverstatedata"]
old-location: display\dd_getdriverstatedata.htm
tech.root: display
ms.assetid: a8b02b56-1733-467b-bd11-0185e6778d34
ms.date: 12/05/2018
ms.keywords: '*PDD_GETDRIVERSTATEDATA, DD_GETDRIVERSTATEDATA, DD_GETDRIVERSTATEDATA structure [Display Devices], d3dstrct_a7ee9601-b71c-4ff4-8ac5-37b62608d463.xml, ddrawint/DD_GETDRIVERSTATEDATA, display.dd_getdriverstatedata'
req.header: ddrawint.h
req.include-header: Winddi.h D3dhal.h, D3dtypes.h
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
req.typenames: '*PDD_GETDRIVERSTATEDATA, DD_GETDRIVERSTATEDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_GETDRIVERSTATEDATA
 - ddrawint/_DD_GETDRIVERSTATEDATA
 - PDD_GETDRIVERSTATEDATA
 - ddrawint/PDD_GETDRIVERSTATEDATA
 - DD_GETDRIVERSTATEDATA
 - ddrawint/DD_GETDRIVERSTATEDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_GETDRIVERSTATEDATA
---

# DD_GETDRIVERSTATEDATA structure


## -description

The DD_GETDRIVERSTATEDATA structure describes the state of the driver.

## -struct-fields

### -field dwFlags

Specifies the set of flags to indicate the data requested. This parameter can be set to one of the following flags:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
D3DDEVINFOID_D3DTEXTUREMANAGER

</td>
<td>
Requests texture-management information performed by the Direct3D runtime in a D3DDEVINFO_TEXTUREMANAGER structure.

</td>
</tr>
<tr>
<td>
D3DDEVINFOID_TEXTUREMANAGER

</td>
<td>
Requests texture-management information performed by either the driver or the Direct3D runtime in a D3DDEVINFO_TEXTUREMANAGER structure.

</td>
</tr>
<tr>
<td>
D3DDEVINFOID_TEXTURING

</td>
<td>
Requests texture-activity information of the application in a D3DDEVINFO_TEXTURING structure.

</td>
</tr>
<tr>
<td>
D3DDEVINFOID_VCACHE

</td>
<td>

<dl>
<dt>DirectX 8.1 versions only</dt>
<dt>Requests vertex-cache information in a D3DDEVINFO_VCACHE structure.</dt>
</dl>


</td>
</tr>
</table>

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure describing the device.

### -field dwhContext

Specifies the ID of the context that information is being requested for.

### -field lpdwStates

Points to the Direct3D driver state data to be filled in by the driver. If, for example, D3DDEVINFOID_VCACHE is specified in the <b>dwFlags</b> member, the driver points the <b>lpdwStates</b> member to a D3DDEVINFO_VCACHE structure that contains vertex-cache information.

### -field dwLength

Specifies the length, in bytes, of the state data to be filled in by the driver.

### -field ddRVal

Specifies the location where the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverstate">D3dGetDriverState</a> callback. A return code of D3D_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-codes-for-direct3d-driver-callbacks">Return Codes for Direct3D Driver Callbacks</a>.

## -remarks

Applications can use the <b>IDirect3DDevice7::GetInfo</b> method and specify the D3DDEVINFOID_D3DTEXTUREMANAGER, D3DDEVINFOID_TEXTUREMANAGER, and D3DDEVINFOID_TEXTURING flags to retrieve texturing information. For more information about this method and the structures related to these flags, see the DirectX SDK documentation. The runtime then passes these flags to the driver.

<b>DirectX 8.1 versions only.</b>The Direct3D runtime specifies the D3DDEVINFOID_VCACHE flag in the <b>dwFlags</b> member to retrieve vertex-cache information from the driver specified at the <b>lpDD</b> member. The driver specifies this information in a D3DDEVINFO_VCACHE structure and returns it at the <b>lpdwStates</b> member. 

<b>DirectX 9.0 and later versions only.</b> The Direct3D runtime asynchronously queries the driver for vertex-cache information by using the D3DDP2OP_CREATEQUERY and D3DDP2OP_ISSUEQUERY commands and the D3DQUERYTYPE_VCACHE query type in calls to the driver's <a href="/windows-hardware/drivers/ddi/content/d3dhal/nc-d3dhal-lpd3dhal_drawprimitives2cb">D3dDrawPrimitives2</a> callback. For more information, see <a href="/windows-hardware/drivers/ddi/content/d3d9types/ns-d3d9types-_d3ddevinfo_vcache">D3DDEVINFO_VCACHE</a>.

<div class="alert"><b>Note</b>  The D3DDEVINFOID_VCACHE flag is defined in d3dhal.h; the other flags that can be set in <b>dwFlags</b> are defined in d3dtypes.h.</div>
<div> </div>

## -see-also

<a href="/windows-hardware/drivers/ddi/content/d3d9types/ns-d3d9types-_d3ddevinfo_vcache">D3DDEVINFO_VCACHE</a>



D3DDP2OP_CREATEQUERY



D3DDP2OP_ISSUEQUERY



<a href="/windows-hardware/drivers/ddi/content/d3dhal/nc-d3dhal-lpd3dhal_drawprimitives2cb">D3dDrawPrimitives2</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverstate">D3dGetDriverState</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a>