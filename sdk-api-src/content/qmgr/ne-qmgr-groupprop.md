---
UID: NE:qmgr.GROUPPROP
title: GROUPPROP
author: windows-sdk-content
description: The GROUPPROP enumeration defines the constant values for retrieving and setting group property values.
old-location: bits\groupprop.htm
old-project: bits
ms.assetid: 8bd5d1df-237a-4c42-afe1-6540ab1ad8c1
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GROUPPROP, GROUPPROP enumeration [BITS], GROUPPROP_DESCRIPTION, GROUPPROP_DISPLAYNAME, GROUPPROP_LOCALUSERID, GROUPPROP_LOCALUSERPWD, GROUPPROP_NOTIFYCLSID, GROUPPROP_NOTIFYFLAGS, GROUPPROP_PRIORITY, GROUPPROP_PROGRESSPERCENT, GROUPPROP_PROGRESSSIZE, GROUPPROP_PROGRESSTIME, GROUPPROP_PROTOCOLFLAGS, GROUPPROP_REMOTEUSERID, GROUPPROP_REMOTEUSERPWD, bits.groupprop, qmgr/GROUPPROP, qmgr/GROUPPROP_DESCRIPTION, qmgr/GROUPPROP_DISPLAYNAME, qmgr/GROUPPROP_LOCALUSERID, qmgr/GROUPPROP_LOCALUSERPWD, qmgr/GROUPPROP_NOTIFYCLSID, qmgr/GROUPPROP_NOTIFYFLAGS, qmgr/GROUPPROP_PRIORITY, qmgr/GROUPPROP_PROGRESSPERCENT, qmgr/GROUPPROP_PROGRESSSIZE, qmgr/GROUPPROP_PROGRESSTIME, qmgr/GROUPPROP_PROTOCOLFLAGS, qmgr/GROUPPROP_REMOTEUSERID, qmgr/GROUPPROP_REMOTEUSERPWD
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: qmgr.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: GROUPPROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qmgr.h
api_name:
 - GROUPPROP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# GROUPPROP enumeration


## -description


<p class="CCE_Message">[Queue Manager (QMGR) is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/ce91f87c-8273-4a1c-99e0-ef55e2a50334">Background Intelligent Transfer Service (BITS)</a>.]

The <b>GROUPPROP</b> enumeration defines the constant values for retrieving and setting group property values.


## -enum-fields




### -field GROUPPROP_PRIORITY

Determines when the QMGR processes the group relative to other groups in the queue.

There is only one priority. You must specify a value of 1 when setting this property. The property always returns a value of 1.

Variant data type can be VT_I4, VT_I2, VT_UI4, VT_UI2, VT_INT, or VT_UINT. 


### -field GROUPPROP_REMOTEUSERID

Not supported.


### -field GROUPPROP_REMOTEUSERPWD

Not supported.


### -field GROUPPROP_LOCALUSERID

Not supported.


### -field GROUPPROP_LOCALUSERPWD

Not supported.


### -field GROUPPROP_PROTOCOLFLAGS

Specifies the protocol to use for the download.

You must specify QM_PROTOCOL_HTTP when setting this property.

Variant data type can be VT_I4, VT_I2, VT_UI4, VT_UI2, VT_INT, or VT_UINT. 


### -field GROUPPROP_NOTIFYFLAGS

Specifies the type of event notification to receive for the group. See Remarks.

Variant data type can be VT_I4, VT_I2, VT_UI4, VT_UI2, VT_INT, or VT_UINT. 


### -field GROUPPROP_NOTIFYCLSID

The 	CLSID to activate when an event specified by <b>GROUPPROP_NOTIFYFLAGS</b> occurs. For more details on CLSID activation, see <a href="https://msdn.microsoft.com/d5d22cf6-d9b5-4001-a0ac-f67d59dde779">IBackgroundCopyCallback1</a>.

Variant data type is VT_BSTR. 


### -field GROUPPROP_PROGRESSSIZE

Not supported.


### -field GROUPPROP_PROGRESSPERCENT

Not supported.


### -field GROUPPROP_PROGRESSTIME

Not supported.


### -field GROUPPROP_DISPLAYNAME

Specifies a display name that can be used to identify the group in a user interface. The length of the string is limited to 256 characters, not including the null terminator.

Variant data type is VT_BSTR. 


### -field GROUPPROP_DESCRIPTION

Specifies a description to associate with the group. The length of the string is limited to 1,024 characters, not including the null terminator.

Variant data type is VT_BSTR. 


## -remarks



The <b>GROUPPROP_NOTIFYFLAGS</b> group property can contain one or more of the following notification flags. 

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>QM_NOTIFY_FILE_DONE</td>
<td>Not supported.</td>
</tr>
<tr>
<td>QM_NOTIFY_JOB_DONE</td>
<td>Not supported.</td>
</tr>
<tr>
<td>QM_NOTIFY_GROUP_DONE</td>
<td>Notifies the application through <a href="https://msdn.microsoft.com/88f75a65-8d27-4413-8b00-4caf11fbcc5e">IBackgroundCopyCallback1::OnStatus</a> that the group is complete.</td>
</tr>
<tr>
<td>QM_NOTIFY_DISABLE_NOTIFY</td>
<td>Disables all notifications.</td>
</tr>
<tr>
<td>QM_NOTIFY_USE_PROGRESSEX</td>
<td>Not supported.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  By default, QMGR calls your <a href="https://msdn.microsoft.com/88f75a65-8d27-4413-8b00-4caf11fbcc5e">IBackgroundCopyCallback1::OnStatus</a> method when an error occurs.</div>
<div> </div>


