---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# tagNMREBAR structure


## -description


Contains information used in handling various rebar notifications. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains additional information about the notification. 


### -field dwMask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Set of flags that define which members of this structure contain valid information. This can be one or more of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RBNM_ID"></a><a id="rbnm_id"></a><dl>
<dt><b>RBNM_ID</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>wID</b> member contains valid information. 

</td>
</tr>
<tr>
<td width="40%"><a id="RBNM_LPARAM"></a><a id="rbnm_lparam"></a><dl>
<dt><b>RBNM_LPARAM</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>lParam</b> member contains valid information. 

</td>
</tr>
<tr>
<td width="40%"><a id="RBNM_STYLE"></a><a id="rbnm_style"></a><dl>
<dt><b>RBNM_STYLE</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>fStyle</b> member contains valid information. 

</td>
</tr>
</table>
 


### -field uBand

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Zero-based index of the band affected by the notification. This will be -1 if no band is affected. 


### -field fStyle

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The style of the band. This is one or more of the RBBS_ styles detailed in the 
					<b>fStyle</b> member of the <a href="https://msdn.microsoft.com/67a59093-f387-47e2-b3bf-b12a7707da31">REBARBANDINFO</a> structure. This member is only valid if 
					<b>dwMask</b> contains RBNM_STYLE. 


### -field wID

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Application-defined identifier of the band. This member is only valid if 
					<b>dwMask</b> contains RBNM_ID. 


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

Application-defined value associated with the band. This member is only valid if 
					<b>dwMask</b> contains RBNM_LPARAM. 

