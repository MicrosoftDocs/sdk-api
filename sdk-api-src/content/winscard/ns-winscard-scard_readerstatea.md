---
UID: NS:winscard.__unnamed_struct_0
title: SCARD_READERSTATEA
author: windows-sdk-content
description: Used by functions for tracking smart cards within readers.
old-location: security\scard_readerstate.htm
tech.root: SecAuthN
ms.assetid: 4e9bbed7-f899-4361-a526-029a710d5147
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPSCARD_READERSTATEA, *PSCARD_READERSTATEA, LPSCARD_READERSTATE, LPSCARD_READERSTATE structure pointer [Security], PSCARD_READERSTATE, PSCARD_READERSTATE structure pointer [Security], SCARD_READERSTATE, SCARD_READERSTATE structure [Security], SCARD_READERSTATEA, SCARD_READERSTATEW, SCARD_STATE_ATRMATCH, SCARD_STATE_CHANGED, SCARD_STATE_EMPTY, SCARD_STATE_EXCLUSIVE, SCARD_STATE_IGNORE, SCARD_STATE_INUSE, SCARD_STATE_MUTE, SCARD_STATE_PRESENT, SCARD_STATE_UNAVAILABLE, SCARD_STATE_UNAWARE, SCARD_STATE_UNKNOWN, _smart_scard_readerstate, security.scard_readerstate, winscard/LPSCARD_READERSTATE, winscard/PSCARD_READERSTATE, winscard/SCARD_READERSTATE, winscard/SCARD_READERSTATEA, winscard/SCARD_READERSTATEW"
ms.topic: struct
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCARD_READERSTATEW (Unicode) and SCARD_READERSTATEA (ANSI)
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
 - HeaderDef
api_location:
 - Winscard.h
api_name:
 - SCARD_READERSTATE
 - SCARD_READERSTATEA
 - SCARD_READERSTATEW
product: Windows
targetos: Windows
req.typenames: SCARD_READERSTATEA, *PSCARD_READERSTATEA, *LPSCARD_READERSTATEA
req.redist: 
---

# SCARD_READERSTATEA structure


## -description


The <b>SCARD_READERSTATE</b> structure is used by functions for tracking <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart cards</a> within <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">readers</a>.


## -struct-fields




### -field szReader

A pointer to the name of the reader being monitored.

Set the value of this member to "\\\\?PnP?\\Notification" and the values of all other members to zero to be notified of the arrival of a new smart card reader.


### -field pvUserData

Not used by the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card subsystem</a>. This member is used by the application.


### -field dwCurrentState

Current <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a> of the reader, as seen by the application. This field can take on any of the following values, in combination, as a bitmask. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_UNAWARE"></a><a id="scard_state_unaware"></a><dl>
<dt><b>SCARD_STATE_UNAWARE</b></dt>
</dl>
</td>
<td width="60%">
The application is unaware of the current <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a>, and would like to know. The use of this value results in an immediate return from state transition monitoring services. This is represented by all bits set to zero.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_IGNORE"></a><a id="scard_state_ignore"></a><dl>
<dt><b>SCARD_STATE_IGNORE</b></dt>
</dl>
</td>
<td width="60%">
The application is not interested in this reader, and it should not be considered during monitoring operations. If this bit value is set, all other bits are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_UNAVAILABLE"></a><a id="scard_state_unavailable"></a><dl>
<dt><b>SCARD_STATE_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The application expects that this reader is not available for use. If this bit is set, then all the following bits are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_EMPTY"></a><a id="scard_state_empty"></a><dl>
<dt><b>SCARD_STATE_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
The application expects that there is no card in the reader. If this bit is set, all the following bits are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_PRESENT"></a><a id="scard_state_present"></a><dl>
<dt><b>SCARD_STATE_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The application expects that there is a card in the reader.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_ATRMATCH"></a><a id="scard_state_atrmatch"></a><dl>
<dt><b>SCARD_STATE_ATRMATCH</b></dt>
</dl>
</td>
<td width="60%">
The application expects that there is a card in the reader with an ATR that matches one of the target cards. If this bit is set, SCARD_STATE_PRESENT is assumed. This bit has no meaning to <a href="https://msdn.microsoft.com/94776f3d-e8f0-4062-a766-2cf28cbfd050">SCardGetStatusChange</a> beyond SCARD_STATE_PRESENT.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_EXCLUSIVE"></a><a id="scard_state_exclusive"></a><dl>
<dt><b>SCARD_STATE_EXCLUSIVE</b></dt>
</dl>
</td>
<td width="60%">
The application expects that the card in the reader is allocated for exclusive use by another application. If this bit is set, SCARD_STATE_PRESENT is assumed.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_INUSE"></a><a id="scard_state_inuse"></a><dl>
<dt><b>SCARD_STATE_INUSE</b></dt>
</dl>
</td>
<td width="60%">
The application expects that the card in the reader is in use by one or more other applications, but may be connected to in shared mode. If this bit is set, SCARD_STATE_PRESENT is assumed.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_MUTE"></a><a id="scard_state_mute"></a><dl>
<dt><b>SCARD_STATE_MUTE</b></dt>
</dl>
</td>
<td width="60%">
The application expects that there is an unresponsive card in the reader.

</td>
</tr>
</table>
 


### -field dwEventState

Current <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a> of the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader</a>, as known by the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card </a><a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager</a>. This field can take on any of the following values, in combination, as a bitmask. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_IGNORE"></a><a id="scard_state_ignore"></a><dl>
<dt><b>SCARD_STATE_IGNORE</b></dt>
</dl>
</td>
<td width="60%">
This reader should be ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_CHANGED"></a><a id="scard_state_changed"></a><dl>
<dt><b>SCARD_STATE_CHANGED</b></dt>
</dl>
</td>
<td width="60%">
There is a difference between the state believed by the application, and the state known by the resource manager. When this bit is set, the application may assume a significant state change has occurred on this reader.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_UNKNOWN"></a><a id="scard_state_unknown"></a><dl>
<dt><b>SCARD_STATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The given reader name is not recognized by the resource manager. If this bit is set, then SCARD_STATE_CHANGED and SCARD_STATE_IGNORE will also be set.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_UNAVAILABLE"></a><a id="scard_state_unavailable"></a><dl>
<dt><b>SCARD_STATE_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The actual state of this reader is not available. If this bit is set, then all the following bits are clear.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_EMPTY"></a><a id="scard_state_empty"></a><dl>
<dt><b>SCARD_STATE_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
There is no card in the reader. If this bit is set, all the following bits will be clear.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_PRESENT"></a><a id="scard_state_present"></a><dl>
<dt><b>SCARD_STATE_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
There is a card in the reader.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_ATRMATCH"></a><a id="scard_state_atrmatch"></a><dl>
<dt><b>SCARD_STATE_ATRMATCH</b></dt>
</dl>
</td>
<td width="60%">
There is a card in the reader with an ATR matching one of the target cards. If this bit is set, SCARD_STATE_PRESENT will also be set. This bit is only returned on the <a href="https://msdn.microsoft.com/7ee90188-6fe5-417b-a7c7-9c29d9cdd4d0">SCardLocateCards</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_EXCLUSIVE"></a><a id="scard_state_exclusive"></a><dl>
<dt><b>SCARD_STATE_EXCLUSIVE</b></dt>
</dl>
</td>
<td width="60%">
The card in the reader is allocated for exclusive use by another application. If this bit is set, SCARD_STATE_PRESENT will also be set.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_INUSE"></a><a id="scard_state_inuse"></a><dl>
<dt><b>SCARD_STATE_INUSE</b></dt>
</dl>
</td>
<td width="60%">
The card in the reader is in use by one or more other applications, but may be connected to in shared mode. If this bit is set, SCARD_STATE_PRESENT will also be set.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_MUTE"></a><a id="scard_state_mute"></a><dl>
<dt><b>SCARD_STATE_MUTE</b></dt>
</dl>
</td>
<td width="60%">
There is an unresponsive card in the reader.

</td>
</tr>
</table>
 


### -field cbAtr

Number of bytes in the returned ATR.


### -field rgbAtr

ATR of the inserted card, with extra alignment bytes.


## -see-also




<a href="https://msdn.microsoft.com/94776f3d-e8f0-4062-a766-2cf28cbfd050">SCardGetStatusChange</a>



<a href="https://msdn.microsoft.com/7ee90188-6fe5-417b-a7c7-9c29d9cdd4d0">SCardLocateCards</a>
 

 

