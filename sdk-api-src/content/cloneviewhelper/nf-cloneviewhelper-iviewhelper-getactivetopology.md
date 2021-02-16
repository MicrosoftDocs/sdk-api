---
UID: NF:cloneviewhelper.IViewHelper.GetActiveTopology
title: IViewHelper::GetActiveTopology (cloneviewhelper.h)
description: The GetActiveTopology method retrieves, for a given adapter, an array of identifiers for targets that are active on a given source.
helpviewer_keywords: ["GetActiveTopology","GetActiveTopology method [Display Devices]","GetActiveTopology method [Display Devices]","IViewHelper interface","IViewHelper interface [Display Devices]","GetActiveTopology method","IViewHelper.GetActiveTopology","IViewHelper::GetActiveTopology","TMM_Ref_584d74ec-d61d-4119-87c6-94de6b568a6f.xml","cloneviewhelper/IViewHelper::GetActiveTopology","display.iviewhelper_getactivetopology"]
old-location: display\iviewhelper_getactivetopology.htm
tech.root: display
ms.assetid: 9862cbf4-26d7-440c-a1eb-bd8decd257c0
ms.date: 12/05/2018
ms.keywords: GetActiveTopology, GetActiveTopology method [Display Devices], GetActiveTopology method [Display Devices],IViewHelper interface, IViewHelper interface [Display Devices],GetActiveTopology method, IViewHelper.GetActiveTopology, IViewHelper::GetActiveTopology, TMM_Ref_584d74ec-d61d-4119-87c6-94de6b568a6f.xml, cloneviewhelper/IViewHelper::GetActiveTopology, display.iviewhelper_getactivetopology
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
 - IViewHelper::GetActiveTopology
 - cloneviewhelper/IViewHelper::GetActiveTopology
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
 - IViewHelper.GetActiveTopology
---

# IViewHelper::GetActiveTopology


## -description

The <b>GetActiveTopology</b> method retrieves, for a given adapter, an array of identifiers for targets that are active on a given source.

## -parameters

### -param wszAdaptorName [in]

[in] A NULL-terminated string that indicates the name of the adapter to retrieve identifiers for. The adapter name is obtained from the <b>DeviceKey</b> member of the DISPLAY_DEVICE structure. The adapter name was set in and returned from a call to the <b>EnumDisplayDevices</b> function. For more information about DISPLAY_DEVICE and <b>EnumDisplayDevices</b>, see the Microsoft Windows SDK documentation.

### -param ulSourceID [in]

[in] A ULONG that is set to the source identifier whose configuration <b>GetActiveTopology</b> retrieves.

### -param pulCount [in, out]

[in,out] A pointer to a variable that receives the number of active target entries in the array that will be subsequently returned in the buffer that <i>pulTargetID</i> points to. For more information about how array entries are retrieved, see the Remarks section.

### -param pulTargetID [in, out]

[in,out] A pointer to a buffer that receives the array of identifiers for the active targets.

## -returns

The <b>GetActiveTopology</b> method returns one of the following values: 

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
<b>GetActiveTopology</b> successfully retrieved identifiers. 

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
<dt><b>ERROR_GRAPHICS_INVALID_VIDEO_PRESENT_SOURCE </b></dt>
</dl>
</td>
<td width="60%">
The source identifier that is specified in the <i>ulSourceID</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_GRAPHICS_INVALID_DISPLAY_ADAPTER </b></dt>
</dl>
</td>
<td width="60%">
<b>GetActiveTopology</b> could not match the adapter name in the <i>wszAdaptorName</i> string to an existing graphics adapter's name. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_GRAPHICS_OPM_PARAMETER_ARRAY_TOO_SMALL </b></dt>
</dl>
</td>
<td width="60%">
The array that was passed in the <i>pulTargetID</i> parameter cannot hold all of the data that <b>GetActiveTopology</b> must insert. TMM will then query for the number of array elements again. 

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

<b>GetActiveTopology</b> is used to record the configuration that TMM will subsequently use in a call to the <a href="/previous-versions/windows/hardware/drivers/ff568174(v=vs.85)">IViewHelper::SetActiveTopology</a> method to restore the configuration. 

For a given source identifier and adapter name, TMM calls <b>GetActiveTopology</b> twice. In the first call to <b>GetActiveTopology</b> , the <i>pulTargetID</i> parameter is set to <b>NULL</b>, and the number of entries in the array of active target identifiers is retrieved in the variable that the <i>pulCount</i> parameter points to. In the second call to <b>GetActiveTopology</b>, the number of entries that was retrieved in the first call is passed in the variable that <i>pulCount</i> points to, and an allocated array is passed to <i>pulTargetID</i>. This allocated array receives the identifiers of the active targets. 

TMM calls <b>GetActiveTopology</b> to record the display configuration that TMM will then use to reestablish the display configuration at a later time if a call to the Win32 <b>ChangeDisplaySettingsEx</b> function alone is not sufficient. For example, if a graphics adapter is set with two or more targets that are mapped to the same source (that is, clone view), the adapter name is the string that was obtained from the <b>DeviceKey</b> member of the DISPLAY_DEVICE structure in a call to the <b>EnumDisplayDevices</b> function. For more information about <b>ChangeDisplaySettingsEx</b>, DISPLAY_DEVICE, and <b>EnumDisplayDevices</b>, see the Windows SDK documentation.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff568174(v=vs.85)">IViewHelper::SetActiveTopology</a>