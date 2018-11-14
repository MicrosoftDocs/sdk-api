---
UID: NF:dinputd.IDirectInputJoyConfig8.GetUserValues
title: IDirectInputJoyConfig8::GetUserValues
author: windows-sdk-content
description: The IDirectInputJoyConfig8::GetUserValues method obtains information about user settings for the joystick.
old-location: hid\idirectinputjoyconfig8_getuservalues.htm
tech.root: hid
ms.assetid: b0de6a60-4dab-41a4-a8f7-629dc2795bfe
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetUserValues, GetUserValues method [Human Input Devices], GetUserValues method [Human Input Devices],IDirectInputJoyConfig8 interface, IDirectInputJoyConfig8 interface [Human Input Devices],GetUserValues method, IDirectInputJoyConfig8.GetUserValues, IDirectInputJoyConfig8::GetUserValues, di_ref_91a06462-3eaf-4c52-b6e3-c8598719f048.xml, dinputd/IDirectInputJoyConfig8::GetUserValues, hid.idirectinputjoyconfig8_getuservalues
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dinputd.h
req.include-header: Dinputd.h
req.target-type: Desktop
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dinputd.h
api_name:
 - IDirectInputJoyConfig8.GetUserValues
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dinputd.h
: 
- IDirectInputJoyConfig8.GetUserValues
: 
---

# IDirectInputJoyConfig8::GetUserValues


## -description


The <b>IDirectInputJoyConfig8::GetUserValues </b>method obtains information about user settings for the joystick. 


## -parameters




### -param arg1

Points to a structure that receives information about the user joystick configuration. The caller must initialize the <b>dwSize</b> member of the <a href="https://msdn.microsoft.com/15424c18-c9ae-4058-97b4-f55b56daea72">DIJOYUSERVALUES</a> structure before calling this method. 


### -param arg2

Specifies which members of the DIJOYUSERVALUES structure contain values to be retrieved. There may be zero, one, or more of the following: 





#### DIJU_USERVALUES

Indicates that the user configuration settings (the <b>ruv</b> member of the DIJOYUSERVALUES structure) is being requested. 



#### DIJU_GLOBALDRIVER

Indicates that the global port driver (the <b>wszGlobalDriver</b> member of the DIJOYUSERVALUES structure) is being requested. 

A list of valid global drivers can be obtained by enumerating the list of joystick types. If the joystick type has the JOY_HWS_ISGAMEPORTDRIVER flag set in the <b>dwFlags</b> member of the JOYHWSETTINGS structure, then the <b>wszCallout</b> member of the <a href="https://msdn.microsoft.com/54f52839-59ed-4edd-8d28-e3504f9900d0">DIJOYTYPEINFO</a> structure contains the name of a driver that can be used as a global driver. 



#### DIJU_GAMEPORTEMULATOR

Unused


## -returns



Returns DI_OK if successful; otherwise, returns the following COM error value: 

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
</table>
 



