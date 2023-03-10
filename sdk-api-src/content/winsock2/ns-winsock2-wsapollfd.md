---
UID: NS:winsock2.pollfd
title: WSAPOLLFD (winsock2.h)
description: Stores socket information used by the WSAPoll function.
helpviewer_keywords: ["*LPWSAPOLLFD","*PWSAPOLLFD","LPWSAPOLLFD","LPWSAPOLLFD structure pointer [Winsock]","PWSAPOLLFD","PWSAPOLLFD structure pointer [Winsock]","WSAPOLLFD","WSAPOLLFD structure [Winsock]","winsock.pollfd","winsock2/LPWSAPOLLFD","winsock2/PWSAPOLLFD","winsock2/WSAPOLLFD"]
old-location: winsock\pollfd.htm
tech.root: WinSock
ms.assetid: 88f122ce-e2ca-44ce-bd53-d73d0962e7ef
ms.date: 12/05/2018
ms.keywords: '*LPWSAPOLLFD, *PWSAPOLLFD, LPWSAPOLLFD, LPWSAPOLLFD structure pointer [Winsock], PWSAPOLLFD, PWSAPOLLFD structure pointer [Winsock], WSAPOLLFD, WSAPOLLFD structure [Winsock], winsock.pollfd, winsock2/LPWSAPOLLFD, winsock2/PWSAPOLLFD, winsock2/WSAPOLLFD'
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: WSAPOLLFD, *PWSAPOLLFD, *LPWSAPOLLFD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - pollfd
 - winsock2/pollfd
 - PWSAPOLLFD
 - winsock2/PWSAPOLLFD
 - WSAPOLLFD
 - winsock2/WSAPOLLFD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsock2.h
api_name:
 - WSAPOLLFD
---

# WSAPOLLFD structure


## -description

The <b>WSAPOLLFD</b> structure stores socket information used by the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsapoll">WSAPoll</a> function.

## -struct-fields

### -field fd

Type: <b>SOCKET</b>

The identifier of the socket for which to find status. This parameter is ignored if set to a negative value. See Remarks.

### -field events

Type: <b>short</b>

A set of flags indicating the type of status being requested. This must be one or more of the following.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>POLLPRI</td>
<td>Priority data may be read without blocking. This flag is not supported by the Microsoft Winsock provider.</td>
</tr>
<tr>
<td>POLLRDBAND</td>
<td>Priority band (out-of-band) data can be read without blocking.</td>
</tr>
<tr>
<td>POLLRDNORM</td>
<td>Normal data can be read without blocking.</td>
</tr>
<tr>
<td>POLLWRNORM</td>
<td>Normal data can be written without blocking.</td>
</tr>
</table>
 

The POLLIN flag is defined as the combination of the <b>POLLRDNORM</b>  and <b>POLLRDBAND</b> flag values. The POLLOUT flag is defined as the same as the <b>POLLWRNORM</b>  flag value.

### -field revents

Type: <b>short</b>

A set of flags that indicate, upon return from the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsapoll">WSAPoll</a> function call, the results of the status query. This can a combination of the following flags.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>POLLERR</td>
<td>An error has occurred.</td>
</tr>
<tr>
<td>POLLHUP</td>
<td>A stream-oriented connection was either disconnected or aborted.</td>
</tr>
<tr>
<td>POLLNVAL</td>
<td>An invalid socket was used.</td>
</tr>
<tr>
<td>POLLPRI</td>
<td>Priority data may be read without blocking. This flag is not returned by the Microsoft Winsock provider.</td>
</tr>
<tr>
<td>POLLRDBAND</td>
<td>Priority band (out-of-band) data may be read without blocking.</td>
</tr>
<tr>
<td>POLLRDNORM</td>
<td>Normal data may be read without blocking.</td>
</tr>
<tr>
<td>POLLWRNORM</td>
<td>Normal data may be written without blocking.</td>
</tr>
</table>
 

The POLLIN flag is defined as the combination of the <b>POLLRDNORM</b>  and <b>POLLRDBAND</b> flag values. The POLLOUT flag is defined as the same as the <b>POLLWRNORM</b>  flag value.

For sockets that do not satisfy the status query, and have no error, the <b>revents</b> member is set to zero upon return.

## -remarks

The <b>WSAPOLLFD</b> structure is defined on Windows Vista and later. 

The <b>WSAPOLLFD</b> structure is used by the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsapoll">WSAPoll</a> function to determine the status of one or more sockets. The set of sockets for which status is requested is specified in <i>fdarray</i> parameter, which is an array of <b>WSAPOLLFD</b> structures.  An application sets the appropriate flags in the <b>events</b> member of the <b>WSAPOLLFD</b> structure to specify the type of status requested for each corresponding socket.  The <b>WSAPoll</b> function returns the status of a socket in the <b>revents</b> member of the <b>WSAPOLLFD</b> structure.

If the <b>fd</b> member of the <b>WSAPOLLFD</b> structure is set to a negative value, the structure is ignored by the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsapoll">WSAPoll</a> function call, and the <b>revents</b> member is cleared upon return. This is useful to applications that maintain a fixed  allocation for the <i>fdarray</i> parameter of <b>WSAPoll</b>; such applications need not waste resources compacting elements of the array for unused entries or reallocating memory. It is unnecessary to clear the <b>revents</b> member prior to calling the <b>WSAPoll</b> function.

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsapoll">WSAPoll</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>



<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>