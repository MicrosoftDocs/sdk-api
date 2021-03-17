---
UID: NF:cloneviewhelper.IViewHelper.SetConfiguration
title: IViewHelper::SetConfiguration (cloneviewhelper.h)
description: The SetConfiguration method passes in display data (display modes and topology data) to the underlying user-mode display driver that the driver should set.
helpviewer_keywords: ["IViewHelper interface [Display Devices]","SetConfiguration method","IViewHelper.SetConfiguration","IViewHelper::SetConfiguration","SetConfiguration","SetConfiguration method [Display Devices]","SetConfiguration method [Display Devices]","IViewHelper interface","TMM_Ref_3eec4d30-b77b-4ff5-88eb-a285efd5cf42.xml","cloneviewhelper/IViewHelper::SetConfiguration","display.iviewhelper_setconfiguration"]
old-location: display\iviewhelper_setconfiguration.htm
tech.root: display
ms.assetid: 8ec09950-afb6-43ff-8e05-4c801e49ba4b
ms.date: 12/05/2018
ms.keywords: IViewHelper interface [Display Devices],SetConfiguration method, IViewHelper.SetConfiguration, IViewHelper::SetConfiguration, SetConfiguration, SetConfiguration method [Display Devices], SetConfiguration method [Display Devices],IViewHelper interface, TMM_Ref_3eec4d30-b77b-4ff5-88eb-a285efd5cf42.xml, cloneviewhelper/IViewHelper::SetConfiguration, display.iviewhelper_setconfiguration
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
 - IViewHelper::SetConfiguration
 - cloneviewhelper/IViewHelper::SetConfiguration
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
 - IViewHelper.SetConfiguration
---

# IViewHelper::SetConfiguration


## -description

The <b>SetConfiguration</b> method passes in display data (display modes and topology data) to the underlying user-mode display driver that the driver should set.

## -parameters

### -param pIStream [in, optional]

[in] A pointer to an <b>IStream</b> interface. The <b>IStream</b> object contains display modes and topology data that are formatted by using the data structures in the <i>Cloneviewhelper.h</i> header file. When the <b>Release</b> method of <b>IStream</b> is called, the memory that backs the <b>IStream</b> is freed. TMM will call <b>Release</b> on the <b>IStream</b> interface pointer if <b>SetConfiguration</b> returns an error result. Otherwise, the user-mode display driver should call <b>Release</b>. <b>Release</b> is called to free the memory that was allocated to store the view information. For more information about <b>IStream</b>, see the Microsoft Windows SDK documentation.

### -param pulStatus [out]

[out] A pointer to a ULONG that receives the driver's status after the driver performs the configuration that TMM passed in. The status can be set to one of the following values.
      

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>SETCONFIGURATION_STATUS_APPLIED (0)</td>
<td>The driver applied the configuration that TMM passed in.</td>
</tr>
<tr>
<td>SETCONFIGURATION_STATUS_ADDITIONAL (1)</td>
<td>The driver applied the configuration that TMM passed in along with additional proprietary hardware-vendor settings.</td>
</tr>
<tr>
<td>SETCONFIGURATION_STATUS_OVERRIDDEN (2)</td>
<td>The driver overrode the configuration that TMM passed in and applied proprietary hardware-vendor settings.</td>
</tr>
</table>

## -returns

The <b>SetConfiguration</b> method returns one of the following values: 

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
<b>SetConfiguration</b> successfully set up display data. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER </b></dt>
</dl>
</td>
<td width="60%">
The <i>pIStream</i> parameter is set to <b>NULL</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT </b></dt>
</dl>
</td>
<td width="60%">
The driver failed to apply settings. In this situation, TMM will resume control and apply settings through a call to the Win32 <b>ChangeDisplaySettingsEx</b> function and the <a href="/previous-versions/windows/hardware/drivers/ff568174(v=vs.85)">IViewHelper::SetActiveTopology</a> method. For more information about <b>ChangeDisplaySettingsEx</b>, see the Windows SDK documentation. 

</td>
</tr>
</table>

## -remarks

After <b>SetConfiguration</b> passes display data to the underlying user-mode display driver, the driver can modify or fold in new data before setting the display. 

<b>SetConfiguration</b> is called when TMM must change the display settings and topology to match a known state that was last recorded by TMM. 

The following data structures are used to format the display modes and topology data that the <b>IStream</b> object that the <i>pIStream</i> parameter points to contains:

<ul>
<li>

<a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-sources">Sources</a>


</li>
<li>

<a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-adapter">Adapter</a>


</li>
<li>

<a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-adapters">Adapters</a>


</li>
<li>

<a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-displaymode">DisplayMode</a>


</li>
<li>

<a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-displaymodes">DisplayModes</a>


</li>
</ul>
These structures are defined in the <i>Cloneviewhelper.h</i>.

## -see-also

<a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-adapter">Adapter</a>



<a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-adapters">Adapters</a>



<a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-displaymode">DisplayMode</a>



<a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-displaymodes">DisplayModes</a>



<a href="/previous-versions/windows/hardware/drivers/ff568174(v=vs.85)">IViewHelper::SetActiveTopology</a>



<a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-sources">Sources</a>