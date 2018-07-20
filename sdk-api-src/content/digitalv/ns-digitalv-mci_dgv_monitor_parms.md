---
UID: NS:digitalv.MCI_DGV_MONITOR_PARMS
title: MCI_DGV_MONITOR_PARMS
author: windows-sdk-content
description: The MCI_DGV_MONITOR_PARMS structure contains parameters for the MCI_MONITOR command.
old-location: multimedia\mci_dgv_monitor_parms.htm
old-project: Multimedia
ms.assetid: 606a86fc-fede-43ea-84b2-386f23ca45b1
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: "*LPMCI_DGV_MONITOR_PARMS, MCI_DGV_METHOD_DIRECT, MCI_DGV_METHOD_POST, MCI_DGV_METHOD_PRE, MCI_DGV_MONITOR_FILE, MCI_DGV_MONITOR_INPUT, MCI_DGV_MONITOR_PARMS, MCI_DGV_MONITOR_PARMS structure [Windows Multimedia], _win32_MCI_DGV_MONITOR_PARMS_str, digitalv/MCI_DGV_MONITOR_PARMS, multimedia.mci_dgv_monitor_parms"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: digitalv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MCI_DGV_MONITOR_PARMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Digitalv.h
api_name:
 - MCI_DGV_MONITOR_PARMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MCI_DGV_MONITOR_PARMS structure


## -description



The <b>MCI_DGV_MONITOR_PARMS</b> structure contains parameters for the <a href="https://msdn.microsoft.com/b6c476ef-d1a4-477d-a104-dda10be60915">MCI_MONITOR</a> command.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field dwSource

One of the following flags for the monitor source:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="MCI_DGV_MONITOR_FILE"></a><a id="mci_dgv_monitor_file"></a><dl>
<dt><b>MCI_DGV_MONITOR_FILE</b></dt>
</dl>
</td>
<td width="60%">
The workspace is the presentation source. (This is the default source.) If this flag is used during recording, the recording pauses. If the <a href="https://msdn.microsoft.com/b6c476ef-d1a4-477d-a104-dda10be60915">MCI_MONITOR</a> command changes the presentation source, recording or playing stops and the current position is the value returned by the <a href="https://msdn.microsoft.com/d1c3dff9-c66f-4525-aac1-4a15b43083e7">MCI_STATUS</a> command for the start position.

</td>
</tr>
<tr>
<td width="40%"><a id="MCI_DGV_MONITOR_INPUT"></a><a id="mci_dgv_monitor_input"></a><dl>
<dt><b>MCI_DGV_MONITOR_INPUT</b></dt>
</dl>
</td>
<td width="60%">
The external input is the presentation source. Playback is paused before the input is selected. If the <a href="https://msdn.microsoft.com/b84956d8-01a0-49f6-a96c-2693a25e6f2a">MCI_SETVIDEO</a> command has been enabled using the MCI_SET_ON flag, this flag displays a default hidden window. Device drivers might limit what other device instances can do while monitoring input.

</td>
</tr>
</table>
 


### -field dwMethod

One of the following constants for the type of monitoring:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="MCI_DGV_METHOD_DIRECT"></a><a id="mci_dgv_method_direct"></a><dl>
<dt><b>MCI_DGV_METHOD_DIRECT</b></dt>
</dl>
</td>
<td width="60%">
The device should be configured for optimum display quality during monitoring. Direct monitoring might be incompatible with motion-video recording.

</td>
</tr>
<tr>
<td width="40%"><a id="MCI_DGV_METHOD_POST"></a><a id="mci_dgv_method_post"></a><dl>
<dt><b>MCI_DGV_METHOD_POST</b></dt>
</dl>
</td>
<td width="60%">
The device should show the external input after compression. Post monitoring supports motion-video recording.

</td>
</tr>
<tr>
<td width="40%"><a id="MCI_DGV_METHOD_PRE"></a><a id="mci_dgv_method_pre"></a><dl>
<dt><b>MCI_DGV_METHOD_PRE</b></dt>
</dl>
</td>
<td width="60%">
The device should show the external input prior to compression.

</td>
</tr>
</table>
 


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/b6c476ef-d1a4-477d-a104-dda10be60915">MCI_MONITOR</a>



<a href="https://msdn.microsoft.com/b84956d8-01a0-49f6-a96c-2693a25e6f2a">MCI_SETVIDEO</a>



<a href="https://msdn.microsoft.com/d1c3dff9-c66f-4525-aac1-4a15b43083e7">MCI_STATUS</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 

