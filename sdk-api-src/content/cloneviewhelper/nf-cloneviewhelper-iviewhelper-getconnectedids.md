---
UID: NF:cloneviewhelper.IViewHelper.GetConnectedIDs
title: IViewHelper::GetConnectedIDs (cloneviewhelper.h)
description: The GetConnectedIDs method retrieves, for a given adapter, an array of identifiers for either targets or sources.
helpviewer_keywords: ["GetConnectedIDs","GetConnectedIDs method [Display Devices]","GetConnectedIDs method [Display Devices]","IViewHelper interface","IViewHelper interface [Display Devices]","GetConnectedIDs method","IViewHelper.GetConnectedIDs","IViewHelper::GetConnectedIDs","TMM_Ref_0c676d81-3866-4c7e-91e9-cd986374fa00.xml","cloneviewhelper/IViewHelper::GetConnectedIDs","display.iviewhelper_getconnectedids"]
old-location: display\iviewhelper_getconnectedids.htm
tech.root: display
ms.assetid: ca3dfc5b-0851-4a09-8b5c-25b8c300c2bb
ms.date: 12/05/2018
ms.keywords: GetConnectedIDs, GetConnectedIDs method [Display Devices], GetConnectedIDs method [Display Devices],IViewHelper interface, IViewHelper interface [Display Devices],GetConnectedIDs method, IViewHelper.GetConnectedIDs, IViewHelper::GetConnectedIDs, TMM_Ref_0c676d81-3866-4c7e-91e9-cd986374fa00.xml, cloneviewhelper/IViewHelper::GetConnectedIDs, display.iviewhelper_getconnectedids
req.header: cloneviewhelper.h
req.include-header: Cloneviewhelper.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Windows 7
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
 - IViewHelper::GetConnectedIDs
 - cloneviewhelper/IViewHelper::GetConnectedIDs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - cloneviewhelper.h
api_name:
 - IViewHelper.GetConnectedIDs
---

# IViewHelper::GetConnectedIDs


## -description

The <b>GetConnectedIDs</b> method retrieves, for a given adapter, an array of identifiers for either targets or sources.

## -parameters

### -param wszAdaptorName [in]

[in] A NULL-terminated string that indicates the name of the adapter to retrieve identifiers for. The adapter name is obtained from the <b>DeviceKey</b> member of the DISPLAY_DEVICE structure. The adapter name was set in and returned from a call to the <b>EnumDisplayDevices</b> function. For more information about DISPLAY_DEVICE and <b>EnumDisplayDevices</b>, see the Microsoft Windows SDK documentation.

### -param pulCount [in, out]

[in,out] A pointer to a variable that receives the number of entries in the array that will be subsequently returned in the buffer that <i>pulID</i> points to. For more information about how array entries are retrieved, see the Remarks section.

### -param pulID [in, out]

[in,out] A pointer to a buffer that receives the array of identifiers for the targets or sources.

### -param ulFlags [in]

[in] A flag value that identifies the type of identifiers to retrieve. <i>ulFlags</i> can be set to one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
GETCONNECTEDIDS_TARGET (0)

</td>
<td>
The array that the <i>pulID</i> parameter points to should contain connected (though not necessarily active) targets.

</td>
</tr>
<tr>
<td>
GETCONNECTEDIDS_SOURCE (1)

</td>
<td>
The array that <i>pulID</i> points to should contain available sources.

</td>
</tr>
</table>

## -returns

The <b>GetConnectedIDs</b> method returns one of the following values: 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK </b></dt>
</dl>
</td>
<td width="60%">
<b>GetConnectedIDs</b> successfully retrieved identifiers. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
The <i>ulFlags</i> parameter contained an unknown value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER </b></dt>
</dl>
</td>
<td width="60%">
One or more of the pointer parameters is set to <b>NULL</b> when it should not be set to <b>NULL</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_GRAPHICS_INVALID_DISPLAY_ADAPTER </b></dt>
</dl>
</td>
<td width="60%">
<b>GetConnectedIDs</b> could not match the adapter name in the <i>wszAdaptorName</i> string to an existing graphics adapter's name. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_GRAPHICS_OPM_PARAMETER_ARRAY_TOO_SMALL </b></dt>
</dl>
</td>
<td width="60%">
The array that was passed in the <i>pulID</i> parameter cannot hold all of the data that <b>GetConnectedIDs</b> must insert. TMM will then query for the number of array elements again. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Any other error code (that is defined in <i>Winerror.h</i>) will cause TMM to not act on the retrieved data.</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -remarks

<b>GetConnectedIDs</b> is used to determine if two monitors that are connected to a graphics adapter can be placed into clone view.

 To qualify as a target, a monitor or other display device must be connected to the computer. For example, consider a graphics adapter with a Digital Video Interface (DVI) connector that supports output through DVI analog and DVI digital. <b>GetConnectedIDs</b> reports the target identifier of the DVI analog or DVI digital output connector only if a monitor is plugged into that connector. Therefore, a report of targets is not a report of all of the outputs that are available through the video ports. Rather, it is a report of what is physically attached to the graphics adapter. Each monitor is reported as a target whether the monitor is active or not.

In the first call to <b>GetConnectedIDs</b>, the <i>pulID </i> parameter is set to <b>NULL</b>, and the number of entries in the array of identifiers is retrieved in the variable that the <i>pulCount</i> parameter points to. In the second call to <b>GetConnectedIDs</b>, the number of entries that was retrieved in the first call is passed in the variable that <i>pulCount</i> points to, and an allocated array is passed to <i>pulCount</i>. This allocated array receives the identifiers of the targets or sources. 

<b>GetConnectedIDs</b> is called when a new second monitor is detected. The <a href="/previous-versions/windows/hardware/drivers/ff568174(v=vs.85)">IViewHelper::SetActiveTopology</a> method must then be called to set the display on the adapter to clone view. The adapter name is the string that was obtained from the <b>DeviceKey</b> member of the DISPLAY_DEVICE structure in a call to the <b>EnumDisplayDevices</b> function. For more information about DISPLAY_DEVICE and <b>EnumDisplayDevices</b>, see the Windows SDK documentation.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff568174(v=vs.85)">IViewHelper::SetActiveTopology</a>