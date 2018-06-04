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

# IDirectInputJoyConfig8::GetTypeInfo


## -description


The <b>IDirectInputJoyConfig8::GetTypeInfo </b>method obtains information about a joystick type. 


## -parameters




### -param






#### - dwFlags

Specifies the parts of the DIJOYTYPEINFO structure pointed to by <i>pjti</i> that are to be filled. There may be zero, one, or more of the following: 





#### DITC_REGHWSETTINGS

Indicates that the registry hardware settings for the joystick are being requested. 



#### DITC_CLSIDCONFIG

Indicates that the joystick configuration CLSID is being requested. If the value is all zeros, then there is no custom configuration for this joystick type. 



#### DITC_DISPLAYNAME

Indicates that the display name for the joystick type is being requested. 



#### DITC_CALLOUT

Indicates that the callout for the joystick type is being requested. 


#### - pjti

Points to a structure that receives information about the joystick type. The caller must initialize the <b>dwSize</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538513">DIJOYTYPEINFO</a> structure before calling this method. 


#### - pwszTypeName

Points to the name of the type, previously obtained from a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540987">IDirectInputJoyConfig8::EnumTypes</a>. 


## -returns



Returns DI_OK if successful; otherwise, returns one of the following COM error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_INVALIDPARAM </b></dt>
</dl>
</td>
<td width="60%">
One or more parameters was invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_NOTFOUND </b></dt>
</dl>
</td>
<td width="60%">
The joystick type was not found. 

</td>
</tr>
</table>
 



