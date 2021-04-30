---
UID: NS:faxdev._FAX_SEND
title: FAX_SEND (faxdev.h)
description: The FAX_SEND structure contains information about an outbound fax document.
helpviewer_keywords: ["*PFAX_SEND","FAX_SEND","FAX_SEND structure [Fax Service]","PFAX_SEND","PFAX_SEND structure pointer [Fax Service]","_mfax_fax_send_str","fax._mfax_fax_send_str","faxdev/FAX_SEND","faxdev/PFAX_SEND"]
old-location: fax\_mfax_fax_send_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_8ueq.htm
ms.date: 12/05/2018
ms.keywords: '*PFAX_SEND, FAX_SEND, FAX_SEND structure [Fax Service], PFAX_SEND, PFAX_SEND structure pointer [Fax Service], _mfax_fax_send_str, fax._mfax_fax_send_str, faxdev/FAX_SEND, faxdev/PFAX_SEND'
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
req.typenames: FAX_SEND, *PFAX_SEND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FAX_SEND
 - faxdev/_FAX_SEND
 - PFAX_SEND
 - faxdev/PFAX_SEND
 - FAX_SEND
 - faxdev/FAX_SEND
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
 - FAX_SEND
---

## -description

The <b>FAX_SEND</b> structure contains information about an outbound fax document. The structure contains the name of the file that holds the fax data stream, the name and telephone number of the calling device, and the name and telephone number of the receiving device.

## -struct-fields

### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies, in bytes, the size of the <b>FAX_SEND</b> structure. Before calling the <a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevsend">FaxDevSend</a> function, the fax service sets this member to <b>sizeof</b>(<b>FAX_SEND</b>).

### -field FileName

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode character string that specifies the full path to the file that contains the data stream for an outbound fax document. The data stream is a TIFF Class F file. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-image-format">Fax Image Format</a>.

### -field CallerName

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode character string that specifies the name of the calling device. The FSP will send this name to the remote receiving device when the FSP sends the fax. For more information, see the following Remarks section.

### -field CallerNumber

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode character string that specifies the telephone number of the calling device. (This number is also the TSID.) The FSP will send this number to the remote receiving device when the FSP sends the fax. For more information, see the following Remarks section.

### -field ReceiverName

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode character string that specifies the name of the device that will receive the outbound fax document.

### -field ReceiverNumber

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode character string that specifies the telephone number of the device that will receive the outbound fax document. This is the telephone number that the FSP will dial.

If you specify the <b>CallHandle</b> member, the <b>ReceiverNumber</b> member must be <b>NULL</b>.

### -field Branding

Type: <b>BOOL</b>

Reserved.

### -field CallHandle

Type: <b>HCALL</b>

Reserved; must be set to <b>NULL</b>.

### -field Reserved

Type: <b>DWORD</b>

This member is reserved  by Microsoft. It must be set to zero.

## -remarks

The FSP can reformat the <b>CallerName</b> and <b>CallerNumber</b> members. The FSP can then transmit the reformatted data to the remote sending device as the called subscriber identifier (CSI) to comply with the recommendation of the standards body of the International Telecommunication Union (ITU) from Study Group 8 (SG8). For more information, see the <b>RoutingInfo</b> and <b>CSI</b> members of the <a href="/windows/desktop/api/faxdev/ns-faxdev-fax_dev_status">FAX_DEV_STATUS</a> structure.

The FSP can also use the reformatted data to add a brand to the fax transmission.

## -see-also

<a href="/windows/desktop/api/faxdev/ns-faxdev-fax_dev_status">FAX_DEV_STATUS</a>

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-provider-structures">Fax Service Provider Structures</a>

<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevsend">FaxDevSend</a>

<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a>

<a href="/previous-versions/windows/desktop/fax/-mfax-using-the-fax-service-provider-api">Using the Fax Service Provider API</a>
