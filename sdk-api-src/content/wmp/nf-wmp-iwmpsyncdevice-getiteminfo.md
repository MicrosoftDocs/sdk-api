---
UID: NF:wmp.IWMPSyncDevice.getItemInfo
title: IWMPSyncDevice::getItemInfo (wmp.h)
description: The getItemInfo method retrieves a metadata value from the device.
helpviewer_keywords: ["IWMPSyncDevice interface [Windows Media Player]","getItemInfo method","IWMPSyncDevice.getItemInfo","IWMPSyncDevice::getItemInfo","IWMPSyncDevicegetItemInfo","getItemInfo","getItemInfo method [Windows Media Player]","getItemInfo method [Windows Media Player]","IWMPSyncDevice interface","wmp.iwmpsyncdevice_getiteminfo","wmp/IWMPSyncDevice::getItemInfo"]
old-location: wmp\iwmpsyncdevice_getiteminfo.htm
tech.root: WMP
ms.assetid: a25b91b8-fe14-4fde-8b68-4e61515e0e5c
ms.date: 4/26/2023
ms.keywords: IWMPSyncDevice interface [Windows Media Player],getItemInfo method, IWMPSyncDevice.getItemInfo, IWMPSyncDevice::getItemInfo, IWMPSyncDevicegetItemInfo, getItemInfo, getItemInfo method [Windows Media Player], getItemInfo method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_getiteminfo, wmp/IWMPSyncDevice::getItemInfo
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPSyncDevice::getItemInfo
 - wmp/IWMPSyncDevice::getItemInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPSyncDevice.getItemInfo
---

# IWMPSyncDevice::getItemInfo


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getItemInfo</b> method retrieves a metadata value from the device.

## -parameters

### -param bstrItemName [in]

<b>BSTR</b> containing the metadata item name. The following table lists the supported item names and describes the value that each retrieves.

<table>
<tr>
<th>Name
                </th>
<th>Retrieves
                </th>
</tr>
<tr>
<td>AutoSyncDefaultRules</td>
<td>
Whether automatic synchronization is done according to default rules or custom rules. A value of "True" indicates default rules, and a value of "False" indicates custom rules.

Use of this attribute is permitted only for devices that have a partnership with Windows Media Player.

Requires Windows Media Player 12.

</td>
</tr>
<tr>
<td>BackgroundSyncState</td>
<td>
Whether Windows Media Player is allowed to perform background operations for the device.

The value can be a string (<b>BSTR</b>) representation of a bitwise combination of one or more of the following flags.

<ul>
<li>1 Background synchronization is allowed.</li>
<li>2 Background transcoding is allowed.</li>
</ul>
The value can also be one of the following strings.

<ul>
<li>"0" No background operations are allowed.</li>
<li>"255" All background operations are allowed.</li>
</ul>
The value of this attribute lasts for the lifetime of Windows Media Player, but is not stored in the Windows Media Player library.

Use of this attribute is permitted only for devices that have a partnership with Windows Media Player.

Requires Windows Media Player 12.

</td>
</tr>
<tr>
<td>Connected</td>
<td>Whether the device is currently connected to Windows Media Player. Possible values are "True" and "False".</td>
</tr>
<tr>
<td>FreeSpace</td>
<td>The size, in bytes, of the available device memory.</td>
</tr>
<tr>
<td>FriendlyName</td>
<td>The friendly name for the device.</td>
</tr>
<tr>
<td>LastSyncErrorCount</td>
<td>The number of synchronization errors that occurred during the most recent synchronization.</td>
</tr>
<tr>
<td>LastSyncNoFitCount</td>
<td>The number of media items that would not fit on the device during the most recent synchronization.</td>
</tr>
<tr>
<td>LastSyncTime</td>
<td>The time of the most recent synchronization.</td>
</tr>
<tr>
<td>Name</td>
<td>The name of the device.</td>
</tr>
<tr>
<td>PercentSpaceReserved</td>
<td>Limits the amount of device storage that Windows Media Player uses for file synchronization by specifying a portion of the storage as reserved. The value is the numeric percentage of total storage on the device represented by a string (<b>BSTR</b>). Supported values range from "0" to "95" inclusive.Use of this attribute is permitted only for devices that have a partnership with Windows Media Player.

Requires Windows Media Player 11.

</td>
</tr>
<tr>
<td>PreferredAudio</td>
<td>
A string (<b>BSTR</b>) representation of the numeric identifier of the preferred storage for audio files on the device.  If the device supports hints, the preferred storage is the location specified by the hint. If the device does not support hints, the preferred storage is the largest storage.

Requires Windows Media Player 12.

</td>
</tr>
<tr>
<td>PreferredVideo</td>
<td>
A string (<b>BSTR</b>) representation of the numeric identifier of the preferred storage for video files on the device.  If the device supports hints, the preferred storage is the location specified by the hint. If the device does not support hints, the preferred storage is the largest storage.

Requires Windows Media Player 12.

</td>
</tr>
<tr>
<td>PreferredPhoto</td>
<td>
A string (<b>BSTR</b>) representation of the numeric identifier of the preferred storage for picture files on the device.  If the device supports hints, the preferred storage is the location specified by the hint. If the device does not support hints, the preferred storage is the largest storage.

Requires Windows Media Player 12.

</td>
</tr>
<tr>
<td>SerialNumber</td>
<td>The device serial number.</td>
</tr>
<tr>
<td>SkippedFiles</td>
<td>
Whether the device has any skipped files. A value of "1" indicates that the device has skipped files. A value of "0" indicates that the device does not have any skipped files.

Use of this attribute is permitted only for devices with which Windows Media Player has a partnership.

Requires Windows Media Player 12.

</td>
</tr>
<tr>
<td>SupportsAudio</td>
<td>Whether the device supports audio playback. Possible values are "True" and "False".</td>
</tr>
<tr>
<td>SupportsPhoto</td>
<td>Whether the device supports displaying photos. Possible values are "True" and "False".</td>
</tr>
<tr>
<td>SupportsVideo</td>
<td>Whether the device supports video playback. Possible values are "True" and "False".</td>
</tr>
<tr>
<td>SyncFilter </td>
<td>
The types of files that will be synchronized during the next synchronization session, and an indication of whether content can be acquired from the device during that synchronization session.

The value can be a string (<b>BSTR</b>) representation of a bitwise combination of one or more of the following flags.

<ul>
<li>"1" Music files will be synchronized.</li>
<li>"2"  Video files will be synchronized.</li>
<li>"4"  Picture files will be synchronized.</li>
<li>"8"  Content can be written to the device, but can not be acquired from the device.</li>
</ul>
For example, the string value "5" indicates that music and picture files will be synchronized.

The value can also be one of the following strings.

<ul>
<li>"0xFF"    No filter will be applied to the synchronization session. That is, files of all types will be synchronized, and content can be both written to the device and acquired from the device.</li>
<li>"0x07" Files of all types will be synchronized.</li>
</ul>
This attribute affects only the next synchronization session.

Use of this attribute is permitted only for devices that have a partnership with Windows Media Player.

Requires Windows Media Player 12.

</td>
</tr>
<tr>
<td>SyncIndex</td>
<td>The partnership index for the device. Possible values are the integers 0 through 16.</td>
</tr>
<tr>
<td>SyncItemCount</td>
<td>The count of items synchronized to the device.</td>
</tr>
<tr>
<td>SyncOnConnect</td>
<td>
Whether Windows Media Player will synchronize the device when the device gets connected. A value of "True" indicates that Windows Media Player will synchronize the device, and a value of "False" indicates that Windows Media Player will not synchronize the device.

Use of this attribute is permitted only for devices that have a partnership with Windows Media Player.

Requires Windows Media Player 12.

</td>
</tr>
<tr>
<td>SyncPercentComplete</td>
<td>The progress of synchronization as a percentage.</td>
</tr>
<tr>
<td>SyncRelationship</td>
<td>A number indicating how the device synchronizes with respect to the current instance of Windows Media Player. Possible values are:0, meaning no relationship.

1, meaning manual synchronization.

2, meaning a partnership exists with the current instance of Windows Media Player.

3, meaning a partnership exists with another instance of Windows Media Player.

</td>
</tr>
<tr>
<td>TotalSpace</td>
<td>The size, in bytes, of the total memory for the device.</td>
</tr>
</table>

### -param pbstrVal [out]

Pointer to a <b>BSTR</b> that contains the specified metadata item name.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_PDA_INITIALIZINGDEVICES (0xC00D118D)</b></dt>
</dl>
</td>
<td width="60%">
Windows Media Player is currently busy initializing devices. Please try again later.

</td>
</tr>
</table>

## -remarks

This method cannot retrieve metadata values for devices having the status <b>wmpdsManualDevice</b>.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice">IWMPSyncDevice Interface</a>



<a href="/windows/desktop/WMP/retrieving-device-attributes">Retrieving Device Attributes</a>