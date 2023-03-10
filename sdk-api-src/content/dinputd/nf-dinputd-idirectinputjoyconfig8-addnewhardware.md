---
UID: NF:dinputd.IDirectInputJoyConfig8.AddNewHardware
title: IDirectInputJoyConfig8::AddNewHardware (dinputd.h)
description: The IDirectInputJoyConfig8::AddNewHardware method displays the Add New Hardware dialog box which guides the user through installing a new input device.
helpviewer_keywords: ["AddNewHardware","AddNewHardware method [Human Input Devices]","AddNewHardware method [Human Input Devices]","IDirectInputJoyConfig8 interface","IDirectInputJoyConfig8 interface [Human Input Devices]","AddNewHardware method","IDirectInputJoyConfig8.AddNewHardware","IDirectInputJoyConfig8::AddNewHardware","di_ref_88ea414c-9d33-4669-8f5b-b14c2d0089ef.xml","dinputd/IDirectInputJoyConfig8::AddNewHardware","hid.idirectinputjoyconfig8_addnewhardware"]
old-location: hid\idirectinputjoyconfig8_addnewhardware.htm
tech.root: hid
ms.assetid: 25a00f6a-7971-4d35-a888-ad80159d0e05
ms.date: 12/05/2018
ms.keywords: AddNewHardware, AddNewHardware method [Human Input Devices], AddNewHardware method [Human Input Devices],IDirectInputJoyConfig8 interface, IDirectInputJoyConfig8 interface [Human Input Devices],AddNewHardware method, IDirectInputJoyConfig8.AddNewHardware, IDirectInputJoyConfig8::AddNewHardware, di_ref_88ea414c-9d33-4669-8f5b-b14c2d0089ef.xml, dinputd/IDirectInputJoyConfig8::AddNewHardware, hid.idirectinputjoyconfig8_addnewhardware
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectInputJoyConfig8::AddNewHardware
 - dinputd/IDirectInputJoyConfig8::AddNewHardware
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dinputd.h
api_name:
 - IDirectInputJoyConfig8.AddNewHardware
---

# IDirectInputJoyConfig8::AddNewHardware


## -description

The <b>IDirectInputJoyConfig8::AddNewHardware </b> method displays the <b>Add New Hardware</b> dialog box which guides the user through installing a new input device.

## -parameters

### -param unnamedParam1

Handle to the window that functions as the owner window for the user interface.

### -param unnamedParam2

GUID that specifies the class of the hardware device to be added. DirectInput comes with the following class GUIDs already defined: 





#### GUID_KeyboardClass

Keyboard devices. 



#### GUID_MouseClass

Mouse devices. 



#### GUID_MediaClass

Media devices, including joysticks. 



#### GUID_HIDClass

HID devices.

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
(E_INVALIDARG). One or more parameters was invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_INVALIDCLASSINSTALLER </b></dt>
</dl>
</td>
<td width="60%">
The class installer for the specified device could not be found or is invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_CANCELLED </b></dt>
</dl>
</td>
<td width="60%">
The user canceled the operation. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_BADINF </b></dt>
</dl>
</td>
<td width="60%">
The INF file for the device that the user selected could not be found or is invalid or damaged. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE </b></dt>
</dl>
</td>
<td width="60%">
DirectInput could not determine whether the operation completed successfully. 

</td>
</tr>
</table>

