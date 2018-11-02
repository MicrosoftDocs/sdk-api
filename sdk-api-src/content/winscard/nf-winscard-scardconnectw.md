---
UID: NF:winscard.SCardConnectW
title: SCardConnectW function
author: windows-sdk-content
description: Establishes a connection (using a specific resource manager context) between the calling application and a smart card contained by a specific reader. If no card exists in the specified reader, an error is returned.
old-location: security\scardconnect.htm
tech.root: secauthn
ms.assetid: 389ada98-383f-4b37-bf5d-c40577ef25fd
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 0, SCARD_PROTOCOL_T0, SCARD_PROTOCOL_T1, SCARD_PROTOCOL_UNDEFINED, SCARD_SHARE_DIRECT, SCARD_SHARE_EXCLUSIVE, SCARD_SHARE_SHARED, SCardConnect, SCardConnect function [Security], SCardConnectA, SCardConnectW, _smart_scardconnect, security.scardconnect, winscard/SCardConnect, winscard/SCardConnectA, winscard/SCardConnectW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardConnectW (Unicode) and SCardConnectA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
 - Ext-MS-Win-wlan-scard-l1-1-0.dll
 - Ext-MS-Win-Security-WinSCard-L1-1-0.dll
api_name:
 - SCardConnect
 - SCardConnectA
 - SCardConnectW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SCardConnectW function


## -description


The <b>SCardConnect</b> function establishes a connection (using a specific <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>) between the calling application and a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> contained by a specific reader. If no card exists in the specified reader, an error is returned.


## -parameters




### -param hContext [in]

A handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>.


### -param szReader [in]

The name of the reader that contains the target card.


### -param dwShareMode [in]

A flag that indicates whether other applications may form connections to the card.

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
This application is willing to share the card with other applications.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_SHARE_EXCLUSIVE"></a><a id="scard_share_exclusive"></a><dl>
<dt><b>SCARD_SHARE_EXCLUSIVE</b></dt>
</dl>
</td>
<td width="60%">
This application is not willing to share the card with other applications.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_SHARE_DIRECT"></a><a id="scard_share_direct"></a><dl>
<dt><b>SCARD_SHARE_DIRECT</b></dt>
</dl>
</td>
<td width="60%">
This application is allocating the reader for its private use, and will be controlling it directly. No other applications are allowed access to it.

</td>
</tr>
</table>
 


### -param dwPreferredProtocols [in]

A bitmask of acceptable protocols for the connection. Possible values may be combined with the <b>OR</b> operation.

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
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
This parameter may be zero only if <i>dwShareMode</i> is set to SCARD_SHARE_DIRECT. In this case, no protocol negotiation will be performed by the drivers until an IOCTL_SMARTCARD_SET_PROTOCOL control directive is sent with <a href="https://msdn.microsoft.com/e8c69e61-4e5e-4385-a0f1-9b594c479984">SCardControl</a>.

</td>
</tr>
</table>
 


### -param phCard [out]

A handle that identifies the connection to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> in the designated reader.


### -param pdwActiveProtocol [out]

A flag that indicates the established active protocol.

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
<tr>
<td width="40%"><a id="SCARD_PROTOCOL_UNDEFINED"></a><a id="scard_protocol_undefined"></a><dl>
<dt><b>SCARD_PROTOCOL_UNDEFINED</b></dt>
</dl>
</td>
<td width="60%">
SCARD_SHARE_DIRECT has been specified, so that no protocol negotiation has occurred. It is possible that there is no card in the reader.

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
<tr>
<td width="40%">
<dl>
<dt><b>SCARD_E_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The reader was unable to connect to the card.

</td>
</tr>
</table>
 




## -remarks



The <b>SCardConnect</b> function is a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> and <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader</a> access function. For more information about other access functions, see 
<a href="https://msdn.microsoft.com/37d92491-174b-471e-b36e-46d9285dd404">Smart Card and Reader Access Functions</a>.


#### Examples

The following example creates a connection to a reader. The example assumes that <i>hContext</i> is a valid handle of type <b>SCARDCONTEXT</b> received from a previous call to <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>.


```cpp
SCARDHANDLE     hCardHandle;
LONG            lReturn;
DWORD           dwAP;

lReturn = SCardConnect( hContext, 
                        (LPCTSTR)"Rainbow Technologies SCR3531 0",
                        SCARD_SHARE_SHARED,
                        SCARD_PROTOCOL_T0 | SCARD_PROTOCOL_T1,
                        &hCardHandle,
                        &dwAP );
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardConnect\n");
    exit(1);  // Or other appropriate action.
}

// Use the connection.
// Display the active protocol.
switch ( dwAP )
{
    case SCARD_PROTOCOL_T0:
        printf("Active protocol T0\n"); 
        break;

    case SCARD_PROTOCOL_T1:
        printf("Active protocol T1\n"); 
        break;

    case SCARD_PROTOCOL_UNDEFINED:
    default:
        printf("Active protocol unnegotiated or unknown\n"); 
        break;
}

// Remember to disconnect (by calling SCardDisconnect).
// ...

```





## -see-also




<a href="https://msdn.microsoft.com/e8c69e61-4e5e-4385-a0f1-9b594c479984">SCardControl</a>



<a href="https://msdn.microsoft.com/d087a006-bd2d-4ad7-965b-36ea8d712ec8">SCardDisconnect</a>



<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/c79e5810-c2be-4184-8ac7-c058ccb9308e">SCardReconnect</a>
 

 

