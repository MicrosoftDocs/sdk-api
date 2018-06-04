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

# IWMPSyncDevice2::setItemInfo


## -description



The <b>setItemInfo</b> method specifies an attribute value for a device.




## -parameters




### -param bstrItemName [in]

<b>BSTR</b>
               specifying the name of the attribute on which to set the new value. For supported attribute names, see Remarks.


### -param bstrVal [in]

<b>BSTR</b>
               specifying the new value. For information about supported values, see Remarks.


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
The method succeeded or a partnership exists.

</td>
</tr>
</table>
 




## -remarks



The following table lists the supported attributes.

<table>
<tr>
<th>
              Attribute
            </th>
<th>
              Description
            </th>
</tr>
<tr>
<td>AutoSyncDefaultRules</td>
<td>
Specifies whether automatic synchronization is done according to default rules or custom rules. A value of "true" specifies default rules, and a value of "false" specifies custom rules.

Use of this attribute is permitted only for devices with which Windows Media Player has a partnership.

Requires Windows Media Player 12.

</td>
</tr>
<tr>
<td>BackgroundSyncState</td>
<td>
Specifies whether Windows Media Player is allowed to perform background operations for the device.

The value can be a string (<b>BSTR</b>) representation of a bitwise combination of one or more of the following flags.

<ul>
<li>1 Allow background synchronization.</li>
<li>2 Allow background transcoding.</li>
</ul>
The value can also be one of the following strings.

<ul>
<li>"0" No background operations are allowed.</li>
<li>"255" Allow all background operations.</li>
</ul>
The value of this attribute lasts for the lifetime of Windows Media Player, but is not stored in the Windows Media Player library.

Use of this attribute is permitted only for devices with which Windows Media Player has a partnership.

Requires Windows Media Player 12.

</td>
</tr>
<tr>
<td>IncludeSkippedFiles</td>
<td>
When the user deletes files from the device, Windows Media Player marks those files as skipped and does not include them in future synchronization operations. Setting this attribute instructs Windows Media Player to include skipped files in the next synchronization.

Set the value of this attribute to the empty <b>BSTR</b>.

Use of this attribute is permitted only for devices with which Windows Media Player has a partnership.

Requires Windows Media Player 12.

</td>
</tr>
<tr>
<td>PercentSpaceReserved</td>
<td>
Limits the amount of device storage that Windows Media Player uses for file synchronization by specifying a portion of the storage as reserved. The value is a numeric percentage of total storage on the device represented by a string (<b>BSTR</b>). Supported values range from "0" to "95".

Use of this attribute is permitted only for devices with which Windows Media Player has a partnership.

</td>
</tr>
<tr>
<td>SyncFilter</td>
<td>
Specifies the types of files that will be synchronized during the next synchronization session, and specifies whether content can be acquired from the device during that synchronization session.

The value can be a string (BSTR) representation of a bitwise combination of one or more of the following flags.

<ul>
<li>1  Synchronize music files.</li>
<li>2  Synchronize video files.</li>
<li>4  Synchronize picture files.</li>
<li>8   Content can be written to the device, but cannot be acquired from the device.</li>
</ul>
For example, the string "5" specifies that music and picture files will be synchronized.

The value can also be one of the following strings.

<ul>
<li>"0xFF"  Apply no filter to the synchronization session. That is, synchronize all types of files and allow content to be both written to the device and acquired from the device.</li>
<li>"0x07" Synchronize files of all types.</li>
</ul>
This attribute affects only the next synchronization session.

Use of this attribute is permitted only for devices with which Windows Media Player has a partnership.

Requires Windows Media Player 12.

</td>
</tr>
<tr>
<td>SyncOnConnect</td>
<td>
Specifies whether Windows Media Player should synchronize the device when the device gets conntected. The value "true" specifies that Windows Media Player should synchronize the device, and the value "false" specifies that Windows Media Player should not synchronize the device.

Use of this attribute is permitted only for devices with which Windows Media Player has a partnership.

Requires Windows Media Player 12.

</td>
</tr>
</table>
 

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/b47fc5ea-741d-4e47-baad-afeb659f1079">IWMPSyncDevice2 Interface</a>
 

 

