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

# GetThemeSysBool function


## -description


Retrieves the Boolean value of a system metric.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to theme data.


### -param iBoolId

TBD




#### - iBoolID [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the system Boolean metric desired. May be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TMT_FLATMENUS"></a><a id="tmt_flatmenus"></a><dl>
<dt><b>TMT_FLATMENUS</b></dt>
</dl>
</td>
<td width="60%">
Describes how menus are drawn. If <b>TRUE</b>, menus are drawn without shadows. If <b>FALSE</b>, menus have shadows underneath them.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Value of desired system metric.




## -remarks



If the theme data handle is not a <b>NULL</b> handle, this function returns the desired <b>BOOL</b> from the SysMetrics section of the visual style. If the theme data handle is <b>NULL</b>, this function returns the value of the specified system Boolean.



