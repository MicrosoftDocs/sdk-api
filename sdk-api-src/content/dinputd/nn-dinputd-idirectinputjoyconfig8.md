---
UID: NN:dinputd.IDirectInputJoyConfig8
title: IDirectInputJoyConfig8 (dinputd.h)
description: IDirectInputJoyConfig8 interface contains methods that allow hardware developers who are writing property sheets to write and read information to and from the registry.
old-location: hid\idirectinputjoyconfig8.htm
tech.root: hid
ms.assetid: baae99bf-a826-45d0-bab2-76a5736bd378
ms.date: 12/05/2018
ms.keywords: IDirectInputJoyConfig8, IDirectInputJoyConfig8 interface [Human Input Devices], IDirectInputJoyConfig8 interface [Human Input Devices],described, di_ref_75413607-c6c1-4341-892a-7f313a0ed9d5.xml, dinputd/IDirectInputJoyConfig8, hid.idirectinputjoyconfig8
ms.topic: interface
f1_keywords:
- dinputd/IDirectInputJoyConfig8
dev_langs:
- c++
req.header: dinputd.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dinputd.h
api_name:
- IDirectInputJoyConfig8
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectInputJoyConfig8 interface


## -description


<b>IDirectInputJoyConfig8</b> interface contains methods that allow hardware developers who are writing property sheets 
 to write and read information to and from the registry. If you need to open registry keys, you should use the 
 <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff540995(v=vs.85)">IDirectInputJoyConfig8::OpenConfigKey</a> and 
 <a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-opentypekey">IDirectInputJoyConfig8::OpenTypeKey</a> methods rather 
 than opening registry keys directly. Using either of these methods ensures that the correct registry branch is opened. 
 In addition, the <b>IDirectInputJoyConfig8</b> interface will be supported in future versions of DirectInput when the underlying registry data 
 may be structured differently.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectInputJoyConfig8</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectInputJoyConfig8</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-acquire">IDirectInputJoyConfig8::Acquire</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::Acquire </b>method acquires "joystick configuration mode." Only one application can be in joystick configuration mode at a time; subsequent attempts by other applications  to acquire this mode should receive the error DIERR_OTHERAPPHASPRIO. After entering configuration mode, the application can make alterations to the global joystick configuration settings. The application should check the existing settings before installing the new ones in case another application changed the settings in the interim. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-addnewhardware">IDirectInputJoyConfig8::AddNewHardware</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::AddNewHardware </b>method displays the <b>Add New Hardware</b> dialog box which guides the user through installing a new input device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-addref">IDirectInputJoyConfig8::AddRef</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::AddRef</b> method increases the reference count of the DirectInputJoyConfig object by 1. This method is part of the <b>IUnknown</b> interface inherited by DirectInputJoyConfig. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-deleteconfig">IDirectInputJoyConfig8::DeleteConfig</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::DeleteConfig </b>method deletes configuration information about a joystick. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-deletetype">IDirectInputJoyConfig8::DeleteType</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::DeleteType </b>method removes information about a joystick type. Use this method with caution; it is the caller's responsibility to ensure that no joystick refers to the deleted type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-enumtypes">IDirectInputJoyConfig8::EnumTypes</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::EnumTypes </b>method enumerates the joystick types currently supported by DirectInput. A joystick type describes how DirectInput should communicate with a joystick device. It includes information such as the presence and location of each of the axes and the number of buttons supported by the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-getconfig">IDirectInputJoyConfig8::GetConfig</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::GetConfig </b>method obtains information about a joystick's configuration. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-gettypeinfo">IDirectInputJoyConfig8::GetTypeInfo</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::GetTypeInfo </b>method obtains information about a joystick type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-getuservalues">IDirectInputJoyConfig8::GetUserValues</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::GetUserValues </b>method obtains information about user settings for the joystick. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-openappstatuskey">IDirectInputJoyConfig8::OpenAppStatusKey</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::OpenAppStatusKey </b>method opens the root key of the application status registry keys, and obtains a handle to the key as a return parameter. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-opentypekey">IDirectInputJoyConfig8::OpenTypeKey</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::OpenTypeKey </b>method opens the registry key associated with a joystick type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-queryinterface">IDirectInputJoyConfig8::QueryInterface</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::QueryInterface </b>method determines whether the DirectInputJoyConfig object supports a particular COM interface. If it does, the system increases the reference count for the object by 1, and the application can begin using that interface immediately. This method is part of the <b>IUnknown</b> interface inherited by DirectInputJoyConfig. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-release">IDirectInputJoyConfig8::Release</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::Release </b>method decreases the reference count of the DirectInputJoyConfig object by 1. This method is part of the <b>IUnknown</b> interface inherited by DirectInputJoyConfig.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-sendnotify">IDirectInputJoyConfig8::SendNotify</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::SendNotify </b>method notifies device drivers and applications that changes to the device configuration have been made. An application that changes device configurations must invoke this method after the changes have been made (and before unacquiring the device). 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-setconfig">IDirectInputJoyConfig8::SetConfig</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::SetConfig </b>method creates or redefines configuration information about a joystick. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-setcooperativelevel">IDirectInputJoyConfig8::SetCooperativeLevel</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::SetCooperativeLevel </b>method establishes the cooperation level for the instance of the device. The only cooperative levels supported for the <b>IDirectInputJoyConfig8</b> interface are DISCL_EXCLUSIVE and DISCL_BACKGROUND. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-settypeinfo">IDirectInputJoyConfig8::SetTypeInfo</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::SetTypeInfo </b>method creates a new joystick type or redefines information about an existing joystick type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-setuservalues">IDirectInputJoyConfig8::SetUserValues</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::SetUserValues </b>method sets the user settings for the joystick. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-unacquire">IDirectInputJoyConfig8::Unacquire</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputJoyConfig8::Unacquire </b>method unacquires "joystick configuration mode". 

</td>
</tr>
</table> 

