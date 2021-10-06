---
UID: NF:dinputd.IDirectInputJoyConfig8.EnumTypes
title: IDirectInputJoyConfig8::EnumTypes (dinputd.h)
description: The IDirectInputJoyConfig8::EnumTypes method enumerates the joystick types currently supported by DirectInput.
helpviewer_keywords: ["EnumTypes","EnumTypes method [Human Input Devices]","EnumTypes method [Human Input Devices]","IDirectInputJoyConfig8 interface","IDirectInputJoyConfig8 interface [Human Input Devices]","EnumTypes method","IDirectInputJoyConfig8.EnumTypes","IDirectInputJoyConfig8::EnumTypes","di_ref_085bc431-1a23-4e9d-ae83-03b55ec163b5.xml","dinputd/IDirectInputJoyConfig8::EnumTypes","hid.idirectinputjoyconfig8_enumtypes"]
old-location: hid\idirectinputjoyconfig8_enumtypes.htm
tech.root: hid
ms.assetid: bacca5a8-2323-46d7-b018-cce2f09bb06d
ms.date: 12/05/2018
ms.keywords: EnumTypes, EnumTypes method [Human Input Devices], EnumTypes method [Human Input Devices],IDirectInputJoyConfig8 interface, IDirectInputJoyConfig8 interface [Human Input Devices],EnumTypes method, IDirectInputJoyConfig8.EnumTypes, IDirectInputJoyConfig8::EnumTypes, di_ref_085bc431-1a23-4e9d-ae83-03b55ec163b5.xml, dinputd/IDirectInputJoyConfig8::EnumTypes, hid.idirectinputjoyconfig8_enumtypes
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
 - IDirectInputJoyConfig8::EnumTypes
 - dinputd/IDirectInputJoyConfig8::EnumTypes
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
 - IDirectInputJoyConfig8.EnumTypes
---

# IDirectInputJoyConfig8::EnumTypes


## -description

The <b>IDirectInputJoyConfig8::EnumTypes </b> method enumerates the joystick types currently supported by DirectInput. A joystick type describes how DirectInput should communicate with a joystick device. It includes information such as the presence and location of each of the axes and the number of buttons supported by the device.

## -parameters

### -param unnamedParam1

Points to an application-defined callback function that receives the DirectInput joystick types. See the Remarks section for the function prototype.

### -param unnamedParam2

Specifies a 32-bit application-defined value to be passed to the callback function. This value can be any 32-bit value; it is prototyped as an LPVOID for convenience.

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
</table>

## -remarks

This callback receives DirectInput joystick types as a result of a call to the IDirectInputJoyConfig8::EnumTypes method.


``` syntax


/*
Parameters
pwszTypeName 
Points to the name of the joystick type. A buffer of MAX_JOYSTRING characters is sufficient to hold the type name. The type name should never be shown to the end user; instead, the "display name" should be shown. Use IDirectInputJoyConfig8::GetTypeInfo to obtain the display name of a joystick type. Type names that begin with a pound sign ("#") represent predefined types that cannot be modified or deleted. 

pvRef 
Points to the application-defined value given in the IDirectInputJoyConfig8::EnumTypes method.

Return value
Returns a BOOL value, DIENUM_CONTINUE, to continue the enumeration, or DIENUM_STOP to stop the enumeration. 

*/


BOOL DIEnumJoyTypeProc(
   LPCWSTR pwszTypeName,
   LPVOID  pvRef
);
 



```


