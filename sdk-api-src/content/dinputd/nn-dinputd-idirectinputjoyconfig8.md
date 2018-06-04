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

# IDirectInputJoyConfig8 interface


## -description


<b>IDirectInputJoyConfig8</b> interface contains methods that allow hardware developers who are writing property sheets 
 to write and read information to and from the registry. If you need to open registry keys, you should use the 
 <a href="https://msdn.microsoft.com/library/windows/hardware/ff540995">IDirectInputJoyConfig8::OpenConfigKey</a> and 
 <a href="https://msdn.microsoft.com/library/windows/hardware/ff540997">IDirectInputJoyConfig8::OpenTypeKey</a> methods rather 
 than opening registry keys directly. Using either of these methods ensures that the correct registry branch is opened. 
 In addition, the <b>IDirectInputJoyConfig8</b> interface will be supported in future versions of DirectInput when the underlying registry data 
 may be structured differently.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectInputJoyConfig8</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectInputJoyConfig8</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectInputJoyConfig8</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540978">IDirectInputJoyConfig8::Acquire</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::Acquire </b>method acquires "joystick configuration mode." Only one application can be in joystick configuration mode at a time; subsequent attempts by other applications  to acquire this mode should receive the error DIERR_OTHERAPPHASPRIO. After entering configuration mode, the application can make alterations to the global joystick configuration settings. The application should check the existing settings before installing the new ones in case another application changed the settings in the interim. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540980">IDirectInputJoyConfig8::AddNewHardware</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::AddNewHardware </b>method displays the <b>Add New Hardware</b> dialog box which guides the user through installing a new input device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540981">IDirectInputJoyConfig8::AddRef</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::AddRef</b> method increases the reference count of the DirectInputJoyConfig object by 1. This method is part of the <b>IUnknown</b> interface inherited by DirectInputJoyConfig. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540984">IDirectInputJoyConfig8::DeleteConfig</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::DeleteConfig </b>method deletes configuration information about a joystick. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540986">IDirectInputJoyConfig8::DeleteType</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::DeleteType </b>method removes information about a joystick type. Use this method with caution; it is the caller's responsibility to ensure that no joystick refers to the deleted type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540987">IDirectInputJoyConfig8::EnumTypes</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::EnumTypes </b>method enumerates the joystick types currently supported by DirectInput. A joystick type describes how DirectInput should communicate with a joystick device. It includes information such as the presence and location of each of the axes and the number of buttons supported by the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540988">IDirectInputJoyConfig8::GetConfig</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::GetConfig </b>method obtains information about a joystick's configuration. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540989">IDirectInputJoyConfig8::GetTypeInfo</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::GetTypeInfo </b>method obtains information about a joystick type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540991">IDirectInputJoyConfig8::GetUserValues</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::GetUserValues </b>method obtains information about user settings for the joystick. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540993">IDirectInputJoyConfig8::OpenAppStatusKey</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::OpenAppStatusKey </b>method opens the root key of the application status registry keys, and obtains a handle to the key as a return parameter. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540995">IDirectInputJoyConfig8::OpenConfigKey</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::OpenConfigKey </b>method opens the registry key associated with a joystick configuration. Control panel applications can use this key to store per-joystick persistent information, such as button mappings. Such private information should be kept in a subkey named <b>OEM</b>; do not store private information in the main configuration key. The application should use <b>RegCloseKey</b> to close the registry key. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540997">IDirectInputJoyConfig8::OpenTypeKey</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::OpenTypeKey </b>method opens the registry key associated with a joystick type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541002">IDirectInputJoyConfig8::QueryInterface</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::QueryInterface </b>method determines whether the DirectInputJoyConfig object supports a particular COM interface. If it does, the system increases the reference count for the object by 1, and the application can begin using that interface immediately. This method is part of the <b>IUnknown</b> interface inherited by DirectInputJoyConfig. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541003">IDirectInputJoyConfig8::Release</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::Release </b>method decreases the reference count of the DirectInputJoyConfig object by 1. This method is part of the <b>IUnknown</b> interface inherited by DirectInputJoyConfig.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541005">IDirectInputJoyConfig8::SendNotify</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::SendNotify </b>method notifies device drivers and applications that changes to the device configuration have been made. An application that changes device configurations must invoke this method after the changes have been made (and before unacquiring the device). 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541006">IDirectInputJoyConfig8::SetConfig</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::SetConfig </b>method creates or redefines configuration information about a joystick. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541008">IDirectInputJoyConfig8::SetCooperativeLevel</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::SetCooperativeLevel </b>method establishes the cooperation level for the instance of the device. The only cooperative levels supported for the <b>IDirectInputJoyConfig8</b> interface are DISCL_EXCLUSIVE and DISCL_BACKGROUND. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541010">IDirectInputJoyConfig8::SetTypeInfo</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::SetTypeInfo </b>method creates a new joystick type or redefines information about an existing joystick type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541013">IDirectInputJoyConfig8::SetUserValues</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::SetUserValues </b>method sets the user settings for the joystick. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541015">IDirectInputJoyConfig8::Unacquire</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::Unacquire </b>method unacquires "joystick configuration mode". 

</td>
</tr>
</table> 

