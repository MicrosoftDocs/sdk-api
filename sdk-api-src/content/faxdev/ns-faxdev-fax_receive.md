---
UID: NS:faxdev._FAX_RECEIVE
title: FAX_RECEIVE (faxdev.h)
description: The FAX_RECEIVE structure contains information about an inbound fax document. This information includes the name of the file that will receive the fax data stream, and the name and telephone number of the receiving device.
helpviewer_keywords: ["*PFAX_RECEIVE","FAX_RECEIVE","FAX_RECEIVE structure [Fax Service]","PFAX_RECEIVE","PFAX_RECEIVE structure pointer [Fax Service]","_mfax_fax_receive_str","fax._mfax_fax_receive_str","faxdev/FAX_RECEIVE","faxdev/PFAX_RECEIVE"]
old-location: fax\_mfax_fax_receive_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_7pf6.htm
ms.date: 12/05/2018
ms.keywords: '*PFAX_RECEIVE, FAX_RECEIVE, FAX_RECEIVE structure [Fax Service], PFAX_RECEIVE, PFAX_RECEIVE structure pointer [Fax Service], _mfax_fax_receive_str, fax._mfax_fax_receive_str, faxdev/FAX_RECEIVE, faxdev/PFAX_RECEIVE'
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
req.typenames: FAX_RECEIVE, *PFAX_RECEIVE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FAX_RECEIVE
 - faxdev/_FAX_RECEIVE
 - PFAX_RECEIVE
 - faxdev/PFAX_RECEIVE
 - FAX_RECEIVE
 - faxdev/FAX_RECEIVE
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
 - FAX_RECEIVE
---

## -description

The <b>FAX_RECEIVE</b> structure contains information about an inbound fax document. This information includes the name of the file that will receive the fax data stream, and the name and telephone number of the receiving device.

## -struct-fields

### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_RECEIVE</b> structure. Before calling the <a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevreceive">FaxDevReceive</a> function, the fax service sets this member to <b>sizeof</b>(<b>FAX_RECEIVE</b>). For more information, see the following Remarks section.

### -field FileName

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode character string that specifies the full path to the file in which the FSP must store the data stream of an inbound fax document. The data stream is a TIFF Class F file. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-image-format">Fax Image Format</a>. The fax service creates the file before it calls the <a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevreceive">FaxDevReceive</a> function. The FSP must specify the OPEN_EXISTING flag when opening this file.

### -field ReceiverName

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode character string that specifies the name of the receiving device. The FSP will send the name to the remote sending device after the receiving device receives an inbound fax. For more information, see the following Remarks section.

### -field ReceiverNumber

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode character string that specifies the telephone number of the receiving device. The FSP will send the number to the remote sending device after the receiving device receives an inbound fax. For more information, see the following Remarks section.

### -field Reserved

Type: <b>DWORD</b>

This member is reserved for future use by Microsoft. It must be set to zero.

## -remarks

The FSP must set the <b>ReceiverName</b> and <b>ReceiverNumber</b> members in this structure. The fax service allocates the memory for these strings. The size of the memory the service allocates is equal to <b>sizeof</b>(<b>FAX_RECEIVE</b>) + <b>FAXDEVRECEIVE_SIZE</b>. The FSP must place the strings in the block of memory that follows the <b>FAX_RECEIVE</b> structure. Note that you must allow for the size of the <b>FileName</b> string that follows immediately after the <b>FAX_RECEIVE</b> structure. The <b>ReceiverName</b> and <b>ReceiverNumber</b> members must point to the location of the strings in the memory block. 

The following code sample and diagram illustrate how to fill in the memory that the fax service allocates.


```
PWSTR ReceiverName;
PWSTR ReceiverNumber;

//
// Routine to retrieve the receiver name
//   and receiver number here.

//
// Set the receiver name and receiver number data
//  in the FAX_RECEIVE structure; then
//  copy the data to the appropriate offset.
//
FaxReceive->ReceiverNumber = (LPWSTR) ( (LPBYTE)FaxReceive->FileName + sizeof(WCHAR)*(wcslen(FaxReceive->FileName) + 1));
wcscpy_s(  FaxReceive->ReceiverNumber, ReceiverNumber );

FaxReceive->ReceiverName = (LPWSTR) ( (LPBYTE)FaxReceive->ReceiverNumber+ sizeof(WCHAR)*(wcslen(FaxReceive->ReceiverNumber) + 1));
wcscpy_s(  FaxReceive->ReceiverName, ReceiverName );

```


<img alt="Filling in the memory that the fax service allocates" src="images/faxover.png"/>
The FSP can reformat the <b>ReceiverName</b> and <b>ReceiverNumber</b> members and transmit the reformatted data to the remote sending device as the called subscriber identifier (CSI) to comply with the recommendation of the standards body of the International Telecommunication Union (ITU) from Study Group 8 (SG8). For more information, see the <b>RoutingInfo</b> and <b>CSI</b> members of the <a href="/windows/desktop/api/faxdev/ns-faxdev-fax_dev_status">FAX_DEV_STATUS</a> structure.

## -see-also

<a href="/windows/desktop/api/faxdev/ns-faxdev-fax_dev_status">FAX_DEV_STATUS</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-provider-structures">Fax Service Provider Structures</a>



<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevreceive">FaxDevReceive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-using-the-fax-service-provider-api">Using the Fax Service Provider API</a>