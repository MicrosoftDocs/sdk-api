---
UID: NS:faxdev._FAX_DEV_STATUS
title: FAX_DEV_STATUS (faxdev.h)
description: The FAX_DEV_STATUS structure contains status and identification information about an individual active fax operation.
helpviewer_keywords: ["*PFAX_DEV_STATUS","FAX_DEV_STATUS","FAX_DEV_STATUS structure [Fax Service]","PFAX_DEV_STATUS","PFAX_DEV_STATUS structure pointer [Fax Service]","_mfax_fax_dev_status_str","fax._mfax_fax_dev_status_str","faxdev/FAX_DEV_STATUS","faxdev/PFAX_DEV_STATUS"]
old-location: fax\_mfax_fax_dev_status_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_0wz6.htm
ms.date: 12/05/2018
ms.keywords: '*PFAX_DEV_STATUS, FAX_DEV_STATUS, FAX_DEV_STATUS structure [Fax Service], PFAX_DEV_STATUS, PFAX_DEV_STATUS structure pointer [Fax Service], _mfax_fax_dev_status_str, fax._mfax_fax_dev_status_str, faxdev/FAX_DEV_STATUS, faxdev/PFAX_DEV_STATUS'
req.header: faxdev.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FAX_DEV_STATUS, *PFAX_DEV_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FAX_DEV_STATUS
 - faxdev/_FAX_DEV_STATUS
 - PFAX_DEV_STATUS
 - faxdev/PFAX_DEV_STATUS
 - FAX_DEV_STATUS
 - faxdev/FAX_DEV_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxDev.h
api_name:
 - FAX_DEV_STATUS
---

## -description

The <b>FAX_DEV_STATUS</b> structure contains status and identification information about an individual active fax operation.

## -struct-fields

### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_DEV_STATUS</b> structure. Before responding to the <a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevreportstatus">FaxDevReportStatus</a> function, the FSP must set this member to <b>sizeof</b>(<b>FAX_DEV_STATUS</b>).

### -field StatusId

Type: <b>DWORD</b>

Specifies a fax status code or value. This can be a predefined fax status code (shown following), one of the TAPI <a href="/windows/desktop/Tapi/lineerr--constants">LINEERR_ Constants</a> error codes, or a value that the FSP defines. If the status identifier is provider-defined, the FSP must also supply a value for the <b>StringId</b> member. Following are the predefined fax status codes.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>FS_INITIALIZING</td>
<td>The call is initializing.</td>
</tr>
<tr>
<td>FS_DIALING </td>
<td>The FSP is dialing digits for the call. </td>
</tr>
<tr>
<td>FS_TRANSMITTING </td>
<td>The FSP is transmitting the fax document. </td>
</tr>
<tr>
<td>FS_RECEIVING </td>
<td>The FSP is receiving the fax document. </td>
</tr>
<tr>
<td>FS_COMPLETED </td>
<td>The fax transmission call is complete. </td>
</tr>
<tr>
<td>FS_LINE_UNAVAILABLE </td>
<td>The FSP cannot complete the call because the device is not available. </td>
</tr>
<tr>
<td>FS_BUSY</td>
<td>The FSP received a busy signal. </td>
</tr>
<tr>
<td>FS_NO_ANSWER </td>
<td>The FSP cannot complete the call because the receiving device does not answer. </td>
</tr>
<tr>
<td>FS_BAD_ADDRESS </td>
<td>The FSP cannot complete the call because the destination address is invalid. </td>
</tr>
<tr>
<td>FS_NO_DIAL_TONE </td>
<td>The FSP cannot complete the call because it does not detect a dial tone. </td>
</tr>
<tr>
<td>FS_DISCONNECTED </td>
<td>The call was disconnected by the receiving device.</td>
</tr>
<tr>
<td>FS_FATAL_ERROR </td>
<td>A fatal error has occurred. </td>
</tr>
<tr>
<td>FS_NOT_FAX_CALL </td>
<td>The call is a data call or a voice call. </td>
</tr>
<tr>
<td>FS_CALL_DELAYED </td>
<td>The FSP received a busy signal multiple times. The provider cannot retry because dialing restrictions exist. (Some countries/regions restrict the number of retries when a number is busy.)</td>
</tr>
<tr>
<td>FS_USER_ABORT</td>
<td>The FSP has canceled the transmission. Cancellation can result from a call to the <a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevabortoperation">FaxDevAbortOperation</a> function. FSPs can also provide a UI for cancellation of fax transmissions.</td>
</tr>
<tr>
<td>FS_ANSWERED</td>
<td>The FSP answered the inbound call but is not yet receiving the call. This status indicates to the fax service that the call may not be a fax call.</td>
</tr>
<tr>
<td>FS_CALL_BLACKLISTED </td>
<td>The FSP cannot complete the call because the telephone number is blocked or reserved, for example, a call to 911 or another emergency number. </td>
</tr>
</table>

The fax status codes FS_BAD_ADDRESS, FS_CALL_BLACKLISTED and FS_USER_ABORT will result in no retry attempts. The fax status code FS_LINE_UNAVAILABLE will result in an immediate retry attempt in the case when the line is unavailable because the service lost the connection to the device (TAPI sent LINE_CLOSE, and the FSP reported FS_LINE_UNAVAILABLE). The retry depends on whether the device is detected back online.  All other fax status codes will result in allowing the fax service to manage retry attempts.

### -field StringId

Type: <b>DWORD</b>

Specifies a string resource identifier for the <b>StatusId</b> member if the <b>StatusId</b> is provider-defined. The fax service loads the string from the FSP's image. If <b>StatusId</b> contains a provider-defined status code or value, this member is required. If <b>StatusId</b> contains a predefined status code or value, this member is ignored.

### -field PageCount

Type: <b>DWORD</b>

Specifies the number of the page in the fax transmission that the FSP is receiving. The page count is relative to one.

### -field CSI

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode character string that specifies an identifier of the remote fax device that is connected with the current call to either the <a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevreceive">FaxDevReceive</a> or <a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevsend">FaxDevSend</a> function.
				

If the operation is sending a fax, the identifier specifies the CSID of the remote device; if the operation is receiving a fax, the identifier specifies the TSID of the remote device.

### -field CallerId

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode character string that identifies the calling device that sent the received fax document. This string can include the telephone number of the calling device.

### -field RoutingInfo

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode character string that specifies the routing string for an inbound fax. The string must be of the form:

<code>Canonical-Phone-Number[|Additional-Routing-Info]</code>

where <code>Canonical-Phone-Number</code> is defined in the <a href="/windows/desktop/Tapi/address-ovr">Address</a> topic of the TAPI documentation (see the Canonical Address subheading); and <code>Additional-Routing-Info</code> is the <i>subaddress</i> of a Canonical Address, and uses the subaddress format.

For DID routing, append the specific DID digits to the telephone number prefix. The DID address must be the canonical telephone number that corresponds to the fully qualified telephone number that the sender would have dialed. 

If there is additional routing information, for example, subaddressing or DTMF tones, separate it from the canonical telephone number by a vertical bar character as indicated in the TAPI specification. You can specify multiple recipients.

For more information, see the Dialable Address and Canonical Address subheadings in the Address topic of the TAPI documentation.

### -field ErrorCode

Type: <b>DWORD</b>

Specifies one of the Win32 <a href="/windows/desktop/Debug/system-error-codes">System Error Codes [Base]</a> that the FSP should use to report an error that occurs. The FSP should set this value to NO_ERROR when it is running and after a fax job completes normally.

### -field Reserved

Type: <b>DWORD</b>

This member is reserved  by Microsoft. It must be set to zero.

## -remarks

The FSP must either set all of the members of the <b>FAX_DEV_STATUS</b> structure to the status information for the active fax operation, or set them to zero.

The fax service allocates the memory for the strings pointed to by the <b>CSI</b>, <b>CallerId</b> and <b>RoutingInfo</b> members. The size of the memory the service allocates is equal to sizeof(<b>FAX_DEV_STATUS</b>) + <b>FAXDEVREPORTSTATUS_SIZE</b>. The FSP must place the strings in the block of memory that immediately follows the <b>FAX_DEV_STATUS</b> structure. The <b>CSI</b>, <b>CallerId</b> and <b>RoutingInfo</b> members must point to the location of the strings in the memory block.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-provider-structures">Fax Service Provider Structures</a>

<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevreceive">FaxDevReceive</a>

<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevreportstatus">FaxDevReportStatus</a>

<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevsend">FaxDevSend</a>

<a href="/previous-versions/windows/desktop/fax/-mfax-using-the-fax-service-provider-api">Using the Fax Service Provider API</a>
