---
UID: NS:winfax._FAX_PORT_INFOA
title: FAX_PORT_INFOA (winfax.h)
description: The FAX_PORT_INFO structure describes one fax port. The data includes, among other items, a device identifier, the port's name and current status, and station identifiers. (ANSI)
helpviewer_keywords: ["*PFAX_PORT_INFOA","FAX_PORT_INFO","FAX_PORT_INFO structure [Fax Service]","FAX_PORT_INFOA","FAX_PORT_INFOW","FPF_RECEIVE","FPF_SEND","FPF_VIRTUAL","FPS_ABORTING","FPS_ANSWERED","FPS_AVAILABLE","FPS_BAD_ADDRESS","FPS_BUSY","FPS_CALL_BLACKLISTED","FPS_CALL_DELAYED","FPS_COMPLETED","FPS_DIALING","FPS_DISCONNECTED","FPS_FATAL_ERROR","FPS_HANDLED","FPS_INITIALIZING","FPS_NOT_FAX_CALL","FPS_NO_ANSWER","FPS_NO_DIAL_TONE","FPS_OFFLINE","FPS_RECEIVING","FPS_RINGING","FPS_ROUTING","FPS_SENDING","FPS_UNAVAILABLE","PFAX_PORT_INFO","PFAX_PORT_INFO structure pointer [Fax Service]","_mfax_fax_port_info_str","fax._mfax_fax_port_info_str","winfax/FAX_PORT_INFO","winfax/FAX_PORT_INFOA","winfax/FAX_PORT_INFOW","winfax/PFAX_PORT_INFO"]
old-location: fax\_mfax_fax_port_info_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_81ki.htm
ms.date: 12/05/2018
ms.keywords: '*PFAX_PORT_INFOA, FAX_PORT_INFO, FAX_PORT_INFO structure [Fax Service], FAX_PORT_INFOA, FAX_PORT_INFOW, FPF_RECEIVE, FPF_SEND, FPF_VIRTUAL, FPS_ABORTING, FPS_ANSWERED, FPS_AVAILABLE, FPS_BAD_ADDRESS, FPS_BUSY, FPS_CALL_BLACKLISTED, FPS_CALL_DELAYED, FPS_COMPLETED, FPS_DIALING, FPS_DISCONNECTED, FPS_FATAL_ERROR, FPS_HANDLED, FPS_INITIALIZING, FPS_NOT_FAX_CALL, FPS_NO_ANSWER, FPS_NO_DIAL_TONE, FPS_OFFLINE, FPS_RECEIVING, FPS_RINGING, FPS_ROUTING, FPS_SENDING, FPS_UNAVAILABLE, PFAX_PORT_INFO, PFAX_PORT_INFO structure pointer [Fax Service], _mfax_fax_port_info_str, fax._mfax_fax_port_info_str, winfax/FAX_PORT_INFO, winfax/FAX_PORT_INFOA, winfax/FAX_PORT_INFOW, winfax/PFAX_PORT_INFO'
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FAX_PORT_INFOW (Unicode) and FAX_PORT_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FAX_PORT_INFOA, *PFAX_PORT_INFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FAX_PORT_INFOA
 - winfax/_FAX_PORT_INFOA
 - PFAX_PORT_INFOA
 - winfax/PFAX_PORT_INFOA
 - FAX_PORT_INFOA
 - winfax/FAX_PORT_INFOA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winfax.h
api_name:
 - FAX_PORT_INFO
 - FAX_PORT_INFOA
 - FAX_PORT_INFOW
---

# FAX_PORT_INFOA structure


## -description

The <b>FAX_PORT_INFO</b> structure describes one fax port. The data includes, among other items, a device identifier, the port's name and current status, and station identifiers.

## -struct-fields

### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_PORT_INFO</b> structure. The calling application should ensure that this member is set to <b>sizeof(FAX_PORT_INFO)</b> before it calls the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetporta">FaxSetPort</a> function.

### -field DeviceId

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the permanent line identifier for the fax device of interest.

### -field State

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that is a fax device status code or value. This member can be one of the predefined device status codes shown following.



#### FPS_DIALING

The device is dialing a fax number.



#### FPS_SENDING

The device is sending a fax document.



#### FPS_RECEIVING

The device is receiving a fax document.



#### FPS_COMPLETED

The device has completed sending or receiving a fax transmission.



#### FPS_UNAVAILABLE

The device is not available because it is in use by another application.



#### FPS_BUSY

The device has encountered a busy signal.



#### FPS_NO_ANSWER

The receiving device did not answer the call.



#### FPS_BAD_ADDRESS

The device dialed an invalid fax number.



#### FPS_NO_DIAL_TONE

The sending device cannot complete the call because it does not detect a dial tone.



#### FPS_DISCONNECTED

The fax call was disconnected by the sender or the caller.



#### FPS_FATAL_ERROR

The device encountered a fatal protocol error.



#### FPS_NOT_FAX_CALL

The device has received a data call or a voice call.



#### FPS_CALL_DELAYED

The device delayed a fax call because the sending device received a busy signal multiple times. The device cannot retry the call because dialing restrictions exist. (Some countries/regions restrict the number of retry attempts when a number is busy.) 



#### FPS_CALL_BLACKLISTED

The device could not complete a call because the telephone number was blocked or reserved; emergency numbers such as 911 are blocked.



#### FPS_INITIALIZING

The device is initializing a call.



#### FPS_OFFLINE

The device is offline and unavailable.



#### FPS_RINGING

The device is ringing.



#### FPS_AVAILABLE

The device is available.



#### FPS_ABORTING

The device is aborting a fax job.



#### FPS_ROUTING

The device is routing a received fax document.



#### FPS_ANSWERED

The device answered a new call.



#### FPS_HANDLED

The fax service processed the outbound fax document; the fax service provider will transmit the document.

### -field Flags

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that is a set of bit flags that specify the capability of the fax port. This member can be a combination of the following values.



#### FPF_RECEIVE

The device can receive faxes.



#### FPF_SEND

The device can send faxes.



#### FPF_VIRTUAL

The device is a virtual fax device. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-virtual-fax-devices">Virtual Fax Devices</a>. Note that you cannot set a device to be virtual. When calling <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetporta">FaxGetPort</a>, the <b>FAX_PORT_INFO</b> flag's <b>FPF_VIRTUAL</b> value indicates whether the device is virtual. When calling <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetporta">FaxSetPort</a>, the service will only relate to the <b>FPF_RECEIVE</b> and <b>FPF_SEND</b> values.

### -field Rings

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the number of times an incoming fax call should ring before the specified device answers the call. Possible values are from 0 to 99 inclusive. This value is ignored unless the <b>FPF_RECEIVE</b> port capability bit flag is set.

### -field Priority

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that determines the relative order in which available fax devices send outgoing transmissions. Valid values for this member are 1 through <i>n</i>, where <i>n</i> is the value of the <i>PortsReturned</i> parameter returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumportsa">FaxEnumPorts</a> function. 

                    

When the fax server initiates an outgoing fax transmission, it attempts to select the device with the highest priority and <b>FPF_SEND</b> port capability. If that device is not available, the server selects the next available device that follows in rank order, and so on. The value of the <b>Priority</b> member has no effect on incoming transmissions.

### -field DeviceName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the name of the fax device of interest.

### -field Tsid

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the TSID. This identifier is usually a telephone number. Only printable characters such as English letters, numeric symbols, and punctuation marks (ASCII range 0x20 to 0x7F) can be used in a TSID.

### -field Csid

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the called station identifier (CSID). This identifier is usually a telephone number. Only printable characters such as English letters, numeric symbols, and punctuation marks (ASCII range 0x20 to 0x7F) can be used in a CSID.

## -remarks

A fax client application passes the <b>FAX_PORT_INFO</b> structure in a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetporta">FaxSetPort</a> function to modify the configuration of the fax port of interest.

If an application calls the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumportsa">FaxEnumPorts</a> function to enumerate all the fax devices currently attached to a fax server, the function returns an array of <b>FAX_PORT_INFO</b> structures. Each structure describes one device in detail. If an application calls the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetporta">FaxGetPort</a> function to query one device, that function returns information about the device in one <b>FAX_PORT_INFO</b> structure. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-ports">Fax Ports</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-fax-device-management">Fax Device Management</a>.





> [!NOTE]
> The winfax.h header defines FAX_PORT_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-structures">Fax Service Client API Structures</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumportsa">FaxEnumPorts</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetporta">FaxGetPort</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetporta">FaxSetPort</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-virtual-fax-devices">Virtual Fax Devices</a>
