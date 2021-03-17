---
UID: NF:cloneviewhelper.IViewHelper.SetActiveTopology
title: IViewHelper::SetActiveTopology (cloneviewhelper.h)
description: The SetActiveTopology method sets up the topology to be used by a Video Present Network (VidPN) on a particular graphics adapter.
helpviewer_keywords: ["IViewHelper interface [Display Devices]","SetActiveTopology method","IViewHelper.SetActiveTopology","IViewHelper::SetActiveTopology","SetActiveTopology","SetActiveTopology method [Display Devices]","SetActiveTopology method [Display Devices]","IViewHelper interface","TMM_Ref_2624b29c-5a04-4312-b65c-9878af440c39.xml","cloneviewhelper/IViewHelper::SetActiveTopology","display.iviewhelper_setactivetopology"]
old-location: display\iviewhelper_setactivetopology.htm
tech.root: display
ms.assetid: a4a9d98c-834b-4578-9ba3-7c7295989a84
ms.date: 12/05/2018
ms.keywords: IViewHelper interface [Display Devices],SetActiveTopology method, IViewHelper.SetActiveTopology, IViewHelper::SetActiveTopology, SetActiveTopology, SetActiveTopology method [Display Devices], SetActiveTopology method [Display Devices],IViewHelper interface, TMM_Ref_2624b29c-5a04-4312-b65c-9878af440c39.xml, cloneviewhelper/IViewHelper::SetActiveTopology, display.iviewhelper_setactivetopology
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
 - IViewHelper::SetActiveTopology
 - cloneviewhelper/IViewHelper::SetActiveTopology
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
 - IViewHelper.SetActiveTopology
---

# IViewHelper::SetActiveTopology


## -description

The <b>SetActiveTopology</b> method sets up the topology to be used by a Video Present Network (VidPN) on a particular graphics adapter.

## -parameters

### -param wszAdaptorName [in]

[in] A NULL-terminated string that indicates the name of the adapter to set up the topology on. The adapter name is obtained from the <b>DeviceKey</b> member of the DISPLAY_DEVICE structure. The adapter name is set in and returned from a call to the <b>EnumDisplayDevices</b> function. For more information about DISPLAY_DEVICE and <b>EnumDisplayDevices</b>, see the Microsoft Windows SDK documentation.

### -param ulSourceID [in]

[in] A ULONG that is set to the source identifier for the display configuration that <b>SetActiveTopology</b> sets.

### -param ulCount [in]

[in] A ULONG that contains the number of active target entries in the array that <i>pulTargetID</i> specifies.

### -param pulTargetID [in]

[in] An array of identifiers for the active targets.

## -returns

The <b>SetActiveTopology</b> method returns one of the following values: 

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
<b>SetActiveTopology</b> successfully set up the topology. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER </b></dt>
</dl>
</td>
<td width="60%">
The pointer parameter (<i>pulTargetID</i>) is set to <b>NULL</b> when it should not be set to <b>NULL</b>. 

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
<b>SetActiveTopology</b> could not match the adapter name in the <i>wszAdaptorName</i> string to an existing graphics adapter's name. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_GRAPHICS_INVALID_VIDEO_PRESENT_TARGET </b></dt>
</dl>
</td>
<td width="60%">
One or more of the targets that are identified by the entries in the array that <i>pulTargetID</i> specifies are invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_GRAPHICS_PATH_NOT_IN_TOPOLOGY </b></dt>
</dl>
</td>
<td width="60%">
The VidPN cannot establish the topology. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Any other error code (that is defined in <i>Winerror.h</i>) will cause TMM to not restore connections.</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -remarks

<b>SetActiveTopology</b> uses the data that was received from a previous call to the <a href="/previous-versions/windows/hardware/drivers/ff568169(v=vs.85)">IViewHelper::GetActiveTopology</a> method. 

For the topology that the <b>SetActiveTopology</b> parameters specify to take affect, the VidPN must be invalidated through a call to the <a href="/previous-versions/windows/hardware/drivers/ff568167(v=vs.85)">IViewHelper::Commit</a> method. 

<b>SetActiveTopology</b> is used only when a display configuration that cannot be established through a call to the Win32 <b>ChangeDisplaySettingsEx</b> function must be set. For example, for clone view on a graphics adapter, the adapter name is the string that was obtained from the <b>DeviceKey</b> member of the DISPLAY_DEVICE structure in a call to the <b>EnumDisplayDevices</b> function. For more information about <b>ChangeDisplaySettingsEx</b>, DISPLAY_DEVICE, and <b>EnumDisplayDevices</b>, see the Windows SDK documentation.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff568167(v=vs.85)">IViewHelper::Commit</a>



<a href="/previous-versions/windows/hardware/drivers/ff568169(v=vs.85)">IViewHelper::GetActiveTopology</a>