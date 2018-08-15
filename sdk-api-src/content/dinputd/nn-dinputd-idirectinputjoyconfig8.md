---
UID: NN:dinputd.IDirectInputJoyConfig8
title: IDirectInputJoyConfig8
author: windows-sdk-content
description: IDirectInputJoyConfig8 interface contains methods that allow hardware developers who are writing property sheets to write and read information to and from the registry.
old-location: hid\idirectinputjoyconfig8.htm
old-project: hid
ms.assetid: baae99bf-a826-45d0-bab2-76a5736bd378
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IDirectInputJoyConfig8, IDirectInputJoyConfig8 interface [Human Input Devices], IDirectInputJoyConfig8 interface [Human Input Devices],described, di_ref_75413607-c6c1-4341-892a-7f313a0ed9d5.xml, dinputd/IDirectInputJoyConfig8, hid.idirectinputjoyconfig8
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dinputd.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: DIEFFESCAPE, *LPDIEFFESCAPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dinputd.h
api_name:
 - IDirectInputJoyConfig8
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectInputJoyConfig8 interface


## -description


<b>IDirectInputJoyConfig8</b> interface contains methods that allow hardware developers who are writing property sheets 
 to write and read information to and from the registry. If you need to open registry keys, you should use the 
 <a href="https://msdn.microsoft.com/f3e902e1-bc5d-419e-b728-2f9199dacb94">IDirectInputJoyConfig8::OpenConfigKey</a> and 
 <a href="https://msdn.microsoft.com/d747625b-a9e3-41cb-894a-1f62599c62a9">IDirectInputJoyConfig8::OpenTypeKey</a> methods rather 
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
<a href="https://msdn.microsoft.com/1df2eb92-9c55-4371-84c7-a4fb879efb7e">IDirectInputJoyConfig8::Acquire</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::Acquire </b>method acquires "joystick configuration mode." Only one application can be in joystick configuration mode at a time; subsequent attempts by other applications  to acquire this mode should receive the error DIERR_OTHERAPPHASPRIO. After entering configuration mode, the application can make alterations to the global joystick configuration settings. The application should check the existing settings before installing the new ones in case another application changed the settings in the interim. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25a00f6a-7971-4d35-a888-ad80159d0e05">IDirectInputJoyConfig8::AddNewHardware</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::AddNewHardware </b>method displays the <b>Add New Hardware</b> dialog box which guides the user through installing a new input device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04e10558-367e-495c-aa1a-43344f803c8a">IDirectInputJoyConfig8::AddRef</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::AddRef</b> method increases the reference count of the DirectInputJoyConfig object by 1. This method is part of the <b>IUnknown</b> interface inherited by DirectInputJoyConfig. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f589e5f4-e003-4a42-b7e6-10b5b14d1aa6">IDirectInputJoyConfig8::DeleteConfig</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::DeleteConfig </b>method deletes configuration information about a joystick. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e1628c4-1d4f-4751-acac-7a309a99aedb">IDirectInputJoyConfig8::DeleteType</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::DeleteType </b>method removes information about a joystick type. Use this method with caution; it is the caller's responsibility to ensure that no joystick refers to the deleted type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bacca5a8-2323-46d7-b018-cce2f09bb06d">IDirectInputJoyConfig8::EnumTypes</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::EnumTypes </b>method enumerates the joystick types currently supported by DirectInput. A joystick type describes how DirectInput should communicate with a joystick device. It includes information such as the presence and location of each of the axes and the number of buttons supported by the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8e2a702-d33e-48d2-8e1c-49e09e8f560f">IDirectInputJoyConfig8::GetConfig</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::GetConfig </b>method obtains information about a joystick's configuration. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e850c3a4-b2dd-4de5-82e3-5bbd90a7ba15">IDirectInputJoyConfig8::GetTypeInfo</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::GetTypeInfo </b>method obtains information about a joystick type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0de6a60-4dab-41a4-a8f7-629dc2795bfe">IDirectInputJoyConfig8::GetUserValues</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::GetUserValues </b>method obtains information about user settings for the joystick. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9caea40-6570-4756-81a4-91a3aaff302b">IDirectInputJoyConfig8::OpenAppStatusKey</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::OpenAppStatusKey </b>method opens the root key of the application status registry keys, and obtains a handle to the key as a return parameter. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3e902e1-bc5d-419e-b728-2f9199dacb94">IDirectInputJoyConfig8::OpenConfigKey</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::OpenConfigKey </b>method opens the registry key associated with a joystick configuration. Control panel applications can use this key to store per-joystick persistent information, such as button mappings. Such private information should be kept in a subkey named <b>OEM</b>; do not store private information in the main configuration key. The application should use <b>RegCloseKey</b> to close the registry key. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d747625b-a9e3-41cb-894a-1f62599c62a9">IDirectInputJoyConfig8::OpenTypeKey</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::OpenTypeKey </b>method opens the registry key associated with a joystick type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aadd7919-2cb1-4c1e-944d-2ccca2f72b3f">IDirectInputJoyConfig8::QueryInterface</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::QueryInterface </b>method determines whether the DirectInputJoyConfig object supports a particular COM interface. If it does, the system increases the reference count for the object by 1, and the application can begin using that interface immediately. This method is part of the <b>IUnknown</b> interface inherited by DirectInputJoyConfig. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60aff330-3646-4bc8-b7f4-b779a2e0796d">IDirectInputJoyConfig8::Release</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::Release </b>method decreases the reference count of the DirectInputJoyConfig object by 1. This method is part of the <b>IUnknown</b> interface inherited by DirectInputJoyConfig.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ca09ce2-82cc-4aee-be96-5123cb0f1f3a">IDirectInputJoyConfig8::SendNotify</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::SendNotify </b>method notifies device drivers and applications that changes to the device configuration have been made. An application that changes device configurations must invoke this method after the changes have been made (and before unacquiring the device). 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58f413c4-7b4c-47bd-8991-ffe681e96f48">IDirectInputJoyConfig8::SetConfig</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::SetConfig </b>method creates or redefines configuration information about a joystick. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0132194a-ee7b-4aa2-af79-f92071072429">IDirectInputJoyConfig8::SetCooperativeLevel</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::SetCooperativeLevel </b>method establishes the cooperation level for the instance of the device. The only cooperative levels supported for the <b>IDirectInputJoyConfig8</b> interface are DISCL_EXCLUSIVE and DISCL_BACKGROUND. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5649ff3d-b7af-489b-b6d0-1252ee4ceb76">IDirectInputJoyConfig8::SetTypeInfo</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::SetTypeInfo </b>method creates a new joystick type or redefines information about an existing joystick type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e33a73b-0315-43a2-8563-f21a7776921c">IDirectInputJoyConfig8::SetUserValues</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::SetUserValues </b>method sets the user settings for the joystick. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6eb4743-5845-4acd-8526-f2ab562aa24f">IDirectInputJoyConfig8::Unacquire</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::Unacquire </b>method unacquires "joystick configuration mode". 

</td>
</tr>
</table> 

