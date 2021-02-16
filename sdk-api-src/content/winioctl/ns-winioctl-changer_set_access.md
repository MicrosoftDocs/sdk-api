---
UID: NS:winioctl._CHANGER_SET_ACCESS
title: CHANGER_SET_ACCESS
description: Contains information that the IOCTL_CHANGER_SET_ACCESS control code needs to set the state of the device's insert/eject port, door, or keypad.
helpviewer_keywords: ["*PCHANGER_SET_ACCESS","CHANGER_SET_ACCESS","CHANGER_SET_ACCESS structure","EXTEND_IEPORT","LOCK_ELEMENT","PCHANGER_SET_ACCESS","PCHANGER_SET_ACCESS structure pointer","RETRACT_IEPORT","UNLOCK_ELEMENT","_win32_changer_set_access_str","base.changer_set_access_str","winioctl/CHANGER_SET_ACCESS","winioctl/PCHANGER_SET_ACCESS"]
old-location: base\changer_set_access_str.htm
tech.root: base
ms.assetid: 14a687c0-18c0-4504-a49e-7ba1b1525d12
ms.date: 12/05/2018
ms.keywords: '*PCHANGER_SET_ACCESS, CHANGER_SET_ACCESS, CHANGER_SET_ACCESS structure, EXTEND_IEPORT, LOCK_ELEMENT, PCHANGER_SET_ACCESS, PCHANGER_SET_ACCESS structure pointer, RETRACT_IEPORT, UNLOCK_ELEMENT, _win32_changer_set_access_str, base.changer_set_access_str, winioctl/CHANGER_SET_ACCESS, winioctl/PCHANGER_SET_ACCESS'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.typenames: CHANGER_SET_ACCESS, *PCHANGER_SET_ACCESS
req.redist: 
f1_keywords:
 - _CHANGER_SET_ACCESS
 - winioctl/_CHANGER_SET_ACCESS
 - PCHANGER_SET_ACCESS
 - winioctl/PCHANGER_SET_ACCESS
 - CHANGER_SET_ACCESS
 - winioctl/CHANGER_SET_ACCESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - CHANGER_SET_ACCESS
---

# CHANGER_SET_ACCESS structure


## -description

Contains information that the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_set_access">IOCTL_CHANGER_SET_ACCESS</a> control code needs to set the state of the device's insert/eject port, door, or keypad.

## -struct-fields

### -field Element

A 
<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element">CHANGER_ELEMENT</a> structure that represents the changer element. The <b>ElementType</b> member can be one of the following values: ChangerDoor, ChangerIEPort, or ChangerKeypad.

### -field Control

The operation to be performed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EXTEND_IEPORT"></a><a id="extend_ieport"></a><dl>
<dt><b>EXTEND_IEPORT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The element is to be extended. 




Requires that <b>Features0</b> is CHANGER_OPEN_IEPORT.

</td>
</tr>
<tr>
<td width="40%"><a id="LOCK_ELEMENT"></a><a id="lock_element"></a><dl>
<dt><b>LOCK_ELEMENT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The element is to be locked. 




Requires that <b>Features0</b> is CHANGER_LOCK_UNLOCK.

</td>
</tr>
<tr>
<td width="40%"><a id="RETRACT_IEPORT"></a><a id="retract_ieport"></a><dl>
<dt><b>RETRACT_IEPORT</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The element is to be retracted. 




Requires that <b>Features0</b> is CHANGER_CLOSE_IEPORT.

</td>
</tr>
<tr>
<td width="40%"><a id="UNLOCK_ELEMENT"></a><a id="unlock_element"></a><dl>
<dt><b>UNLOCK_ELEMENT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The element is to be unlocked. 




Requires that <b>Features0</b> is CHANGER_LOCK_UNLOCK.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element">CHANGER_ELEMENT</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_set_access">IOCTL_CHANGER_SET_ACCESS</a>