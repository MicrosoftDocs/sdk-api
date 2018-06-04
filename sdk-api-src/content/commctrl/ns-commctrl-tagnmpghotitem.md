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

# tagNMPGHOTITEM structure


## -description


Contains information used with the <a href="https://msdn.microsoft.com/0f59677c-0251-49f4-b909-6fac6d93f354">PGN_HOTITEMCHANGE</a> notification code. 



## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains additional information about the notification. 


### -field idOld

Type: <b>int</b>

Value of type <b>int</b> that specifies the command identifier of the previously highlighted item. 


### -field idNew

Type: <b>int</b>

Value of type <b>int</b> that specifies the command identifier of the highlighted item. 


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

<b>DWORD</b> that contains flags that indicate why the hot item has changed. This can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>HICF_ENTERING</dt>
</dl>
</td>
<td width="60%">
If this flag is set, there is no previous hot item and <b>idOld</b> does not contain valid information.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>HICF_LEAVING</dt>
</dl>
</td>
<td width="60%">
If this flag is set, there is no new hot item and <b>idNew</b> does not contain valid information.

</td>
</tr>
</table>
 

