---
UID: NF:winscard.SCardReconnect
title: SCardReconnect function
author: windows-sdk-content
description: Reestablishes an existing connection between the calling application and a smart card.
old-location: security\scardreconnect.htm
old-project: secauthn
ms.assetid: c79e5810-c2be-4184-8ac7-c058ccb9308e
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: SCARD_LEAVE_CARD, SCARD_PROTOCOL_T0, SCARD_PROTOCOL_T1, SCARD_RESET_CARD, SCARD_SHARE_EXCLUSIVE, SCARD_SHARE_SHARED, SCARD_UNPOWER_CARD, SCardReconnect, SCardReconnect function [Security], _smart_scardreconnect, security.scardreconnect, winscard/SCardReconnect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winscard.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: WINSAT_BITMAP_SIZE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
 - Ext-MS-Win-Security-WinSCard-L1-1-0.dll
api_name:
 - SCardReconnect
product: Windows
targetos: Windows
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SCardReconnect function


## -description


The <b>SCardReconnect</b> function reestablishes an existing connection between the calling application and a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a>. This function moves a card handle from direct access to general access, or acknowledges and clears an error condition that is preventing further access to the card.


## -parameters




### -param hCard [in]

Reference value obtained from a previous call to 
<a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a>.


### -param dwShareMode [in]

Flag that indicates whether other applications may form connections to this card.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_SHARE_SHARED"></a><a id="scard_share_shared"></a><dl>
<dt><b>SCARD_SHARE_SHARED</b></dt>
</dl>
</td>
<td width="60%">
This application will share this card with other applications.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_SHARE_EXCLUSIVE"></a><a id="scard_share_exclusive"></a><dl>
<dt><b>SCARD_SHARE_EXCLUSIVE</b></dt>
</dl>
</td>
<td width="60%">
This application will not share this card with other applications.

</td>
</tr>
</table>
 


### -param dwPreferredProtocols [in]

Bitmask of acceptable protocols for this connection. Possible values may be combined with the <b>OR</b> operation. 



The value of this parameter should include the current protocol. Attempting to reconnect with a protocol other than the current protocol will result in an error.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_PROTOCOL_T0"></a><a id="scard_protocol_t0"></a><dl>
<dt><b>SCARD_PROTOCOL_T0</b></dt>
</dl>
</td>
<td width="60%">
<a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">T=0</a> is an acceptable protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_PROTOCOL_T1"></a><a id="scard_protocol_t1"></a><dl>
<dt><b>SCARD_PROTOCOL_T1</b></dt>
</dl>
</td>
<td width="60%">
<a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">T=1</a> is an acceptable protocol.

</td>
</tr>
</table>
 


### -param dwInitialization [in]

Type of initialization that should be performed on the card.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_LEAVE_CARD"></a><a id="scard_leave_card"></a><dl>
<dt><b>SCARD_LEAVE_CARD</b></dt>
</dl>
</td>
<td width="60%">
Do not do anything special on reconnect.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_RESET_CARD"></a><a id="scard_reset_card"></a><dl>
<dt><b>SCARD_RESET_CARD</b></dt>
</dl>
</td>
<td width="60%">
Reset the card (Warm Reset).

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_UNPOWER_CARD"></a><a id="scard_unpower_card"></a><dl>
<dt><b>SCARD_UNPOWER_CARD</b></dt>
</dl>
</td>
<td width="60%">
Power down the card and reset it (Cold Reset).

</td>
</tr>
</table>
 


### -param pdwActiveProtocol [out, optional]

Flag that indicates the established active protocol.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_PROTOCOL_T0"></a><a id="scard_protocol_t0"></a><dl>
<dt><b>SCARD_PROTOCOL_T0</b></dt>
</dl>
</td>
<td width="60%">
<a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">T=0</a> is the active protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_PROTOCOL_T1"></a><a id="scard_protocol_t1"></a><dl>
<dt><b>SCARD_PROTOCOL_T1</b></dt>
</dl>
</td>
<td width="60%">
<a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">T=1</a> is the active protocol.

</td>
</tr>
</table>
 


## -returns



This function returns different values depending on whether it succeeds or fails.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Success</b></dt>
</dl>
</td>
<td width="60%">
SCARD_S_SUCCESS.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Failure</b></dt>
</dl>
</td>
<td width="60%">
An error code. For more information, see 
<a href="https://msdn.microsoft.com/en-us/library/Aa374738(v=VS.85).aspx">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -remarks



<b>SCardReconnect</b> is a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> and <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader</a> access function. For information about other access functions, see 
<a href="https://msdn.microsoft.com/37d92491-174b-471e-b36e-46d9285dd404">Smart Card and Reader Access Functions</a>.


#### Examples

The following example  shows reestablishing a connection.


```cpp
DWORD     dwAP;
LONG      lReturn;

// Reconnect.
// hCardHandle was set by a previous call to SCardConnect.
lReturn = SCardReconnect(hCardHandle,
                         SCARD_SHARE_SHARED,
                         SCARD_PROTOCOL_T0 | SCARD_PROTOCOL_T1,
                         SCARD_LEAVE_CARD,
                         &dwAP );
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardReconnect\n");

```





## -see-also




<a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a>



<a href="https://msdn.microsoft.com/d087a006-bd2d-4ad7-965b-36ea8d712ec8">SCardDisconnect</a>
 

 

