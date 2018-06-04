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

# IImePadApplet::Notify


## -description


Called from <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> to pass information with a notify code


## -parameters




### -param lpImePad [in]

Pointer of IUnknown interface. To get the <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> interface pointer, use <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a>.


### -param notify [in]

The <a href="https://msdn.microsoft.com/F3BC7176-9659-47B6-AFCA-049807394961">IImePadApplet</a> notify code. See Remarks for the possible codes.


### -param wParam [in, out]

Additional information specific to <i>notify</i>.


### -param lParam [in, out]

Additional information specific to <i>notify</i>.


## -returns



<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.




## -remarks



<h3><a id="Possible_notify_codes__IMEPN___values_"></a><a id="possible_notify_codes__imepn___values_"></a><a id="POSSIBLE_NOTIFY_CODES__IMEPN___VALUES_"></a>Possible notify codes (<b>IMEPN_*</b> values)</h3>

<table>
<tr>
<th>Code</th>
<th>Description</th>
</tr>
<tr>
<td><b>IMEPN_ACTIVATE</b></td>
<td>The applet is activated.</td>
</tr>
<tr>
<td><b>IMEPN_INACTIVATE</b></td>
<td>The applet is inactivate.</td>
</tr>
<tr>
<td><b>IMEPN_SHOW</b></td>
<td>IMEPad and the applet are shown.</td>
</tr>
<tr>
<td><b>IMEPN_HIDE</b></td>
<td>IMEPad and the applet are hidden.</td>
</tr>
<tr>
<td><b>IMEPN_SIZECHANGING</b></td>
<td>The applet size is changing.</td>
</tr>
<tr>
<td><b>IMEPN_SIZECHANGED</b></td>
<td>The applet size has changed.</td>
</tr>
<tr>
<td><b>IMEPN_CONFIG</b></td>
<td>The applet setting is selected in IMEPad menu.</td>
</tr>
<tr>
<td><b>IMEPN_HELP</b></td>
<td>The applet help is selected in IMEPad menu.</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/F3BC7176-9659-47B6-AFCA-049807394961">IImePadApplet</a>
 

 

