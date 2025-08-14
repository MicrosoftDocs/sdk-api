---
UID: NF:winscard.SCardConnectW
title: SCardConnectW function (winscard.h)
description: Establishes a connection (using a specific resource manager context) between the calling application and a smart card contained by a specific reader. If no card exists in the specified reader, an error is returned. (Unicode)
helpviewer_keywords: ["0", "SCARD_PROTOCOL_T0", "SCARD_PROTOCOL_T1", "SCARD_PROTOCOL_UNDEFINED", "SCARD_SHARE_DIRECT", "SCARD_SHARE_EXCLUSIVE", "SCARD_SHARE_SHARED", "SCardConnect", "SCardConnect function [Security]", "SCardConnectW", "_smart_scardconnect", "security.scardconnect", "winscard/SCardConnect", "winscard/SCardConnectW"]
old-location: security\scardconnect.htm
tech.root: security
ms.assetid: 389ada98-383f-4b37-bf5d-c40577ef25fd
ms.date: 12/05/2018
ms.keywords: 0, SCARD_PROTOCOL_T0, SCARD_PROTOCOL_T1, SCARD_PROTOCOL_UNDEFINED, SCARD_SHARE_DIRECT, SCARD_SHARE_EXCLUSIVE, SCARD_SHARE_SHARED, SCardConnect, SCardConnect function [Security], SCardConnectA, SCardConnectW, _smart_scardconnect, security.scardconnect, winscard/SCardConnect, winscard/SCardConnectA, winscard/SCardConnectW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SCardConnectW
 - winscard/SCardConnectW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-security-winscard-l1-1-1.dll
 - Winscard.dll
 - Ext-MS-Win-wlan-scard-l1-1-0.dll
 - Ext-MS-Win-Security-WinSCard-L1-1-0.dll
api_name:
 - SCardConnect
 - SCardConnectA
 - SCardConnectW
---

# SCardConnectW function


## -description

The <b>SCardConnect</b> function establishes a connection (using a specific <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>) between the calling application and a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> contained by a specific reader. If no card exists in the specified reader, an error is returned.

## -parameters

### -param hContext [in]

A handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>.

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
<a href="/windows/desktop/SecGloss/t-gly">T=0</a> is an acceptable protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_PROTOCOL_T1"></a><a id="scard_protocol_t1"></a><dl>
<dt><b>SCARD_PROTOCOL_T1</b></dt>
</dl>
</td>
<td width="60%">
<a href="/windows/desktop/SecGloss/t-gly">T=1</a> is an acceptable protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
This parameter may be zero only if <i>dwShareMode</i> is set to SCARD_SHARE_DIRECT. In this case, no protocol negotiation will be performed by the drivers until an IOCTL_SMARTCARD_SET_PROTOCOL control directive is sent with <a href="/windows/desktop/api/winscard/nf-winscard-scardcontrol">SCardControl</a>.

</td>
</tr>
</table>

### -param phCard [out]

A handle that identifies the connection to the <a href="/windows/desktop/SecGloss/s-gly">smart card</a> in the designated reader.

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
<a href="/windows/desktop/SecGloss/t-gly">T=0</a> is the active protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_PROTOCOL_T1"></a><a id="scard_protocol_t1"></a><dl>
<dt><b>SCARD_PROTOCOL_T1</b></dt>
</dl>
</td>
<td width="60%">
<a href="/windows/desktop/SecGloss/t-gly">T=1</a> is the active protocol.

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
<a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.

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

The <b>SCardConnect</b> function is a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> and <a href="/windows/desktop/SecGloss/r-gly">reader</a> access function. For more information about other access functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-and-reader-access-functions">Smart Card and Reader Access Functions</a>.


#### Examples

The following example creates a connection to a reader. The example assumes that <i>hContext</i> is a valid handle of type <b>SCARDCONTEXT</b> received from a previous call to <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>.


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






> [!NOTE]
> The winscard.h header defines SCardConnect as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardcontrol">SCardControl</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scarddisconnect">SCardDisconnect</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardreconnect">SCardReconnect</a>
