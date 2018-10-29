---
UID: NS:faxdev._FAX_RECEIVE
title: "_FAX_RECEIVE"
author: windows-sdk-content
description: The FAX_RECEIVE structure contains information about an inbound fax document. This information includes the name of the file that will receive the fax data stream, and the name and telephone number of the receiving device.
old-location: fax\_mfax_fax_receive_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_7pf6.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PFAX_RECEIVE, FAX_RECEIVE, FAX_RECEIVE structure [Fax Service], PFAX_RECEIVE, PFAX_RECEIVE structure pointer [Fax Service], _FAX_RECEIVE, _mfax_fax_receive_str, fax._mfax_fax_receive_str, faxdev/FAX_RECEIVE, faxdev/PFAX_RECEIVE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxDev.h
api_name:
 - FAX_RECEIVE
product: Windows
targetos: Windows
req.typenames: FAX_RECEIVE, *PFAX_RECEIVE
req.redist: 
---

# _FAX_RECEIVE structure


## -description


The <b>FAX_RECEIVE</b> structure contains information about an inbound fax document. This information includes the name of the file that will receive the fax data stream, and the name and telephone number of the receiving device.


## -struct-fields




### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_RECEIVE</b> structure. Before calling the <a href="https://msdn.microsoft.com/3f37c113-2971-4092-8753-b0d30b8ce6c1">FaxDevReceive</a> function, the fax service sets this member to <b>sizeof</b>(<b>FAX_RECEIVE</b>). For more information, see the following Remarks section.


### -field FileName

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode character string that specifies the full path to the file in which the FSP must store the data stream of an inbound fax document. The data stream is a TIFF Class F file. For more information, see <a href="https://msdn.microsoft.com/d7840c10-6059-40ed-9040-50eefefc7349">Fax Image Format</a>. The fax service creates the file before it calls the <a href="https://msdn.microsoft.com/3f37c113-2971-4092-8753-b0d30b8ce6c1">FaxDevReceive</a> function. The FSP must specify the OPEN_EXISTING flag when opening this file.


### -field ReceiverName

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode character string that specifies the name of the receiving device. The FSP will send the name to the remote sending device after the receiving device receives an inbound fax. For more information, see the following Remarks section.


### -field ReceiverNumber

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode character string that specifies the telephone number of the receiving device. The FSP will send the number to the remote sending device after the receiving device receives an inbound fax. For more information, see the following Remarks section.


### -field Reserved

 




#### - Reserved[4]

Type: <b>DWORD</b>

This member is reserved for future use by Microsoft. It must be set to zero.


## -remarks



The FSP must set the <b>ReceiverName</b> and <b>ReceiverNumber</b> members in this structure. The fax service allocates the memory for these strings. The size of the memory the service allocates is equal to <b>sizeof</b>(<b>FAX_RECEIVE</b>) + <b>FAXDEVRECEIVE_SIZE</b>. The FSP must place the strings in the block of memory that follows the <b>FAX_RECEIVE</b> structure. Note that you must allow for the size of the <b>FileName</b> string that follows immediately after the <b>FAX_RECEIVE</b> structure. The <b>ReceiverName</b> and <b>ReceiverNumber</b> members must point to the location of the strings in the memory block. 

The following code sample and diagram illustrate how to fill in the memory that the fax service allocates.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>PWSTR ReceiverName;
PWSTR ReceiverNumber;

//
// Routine to retrieve the receiver name
//   and receiver number here.

//
// Set the receiver name and receiver number data
//  in the FAX_RECEIVE structure; then
//  copy the data to the appropriate offset.
//
FaxReceive-&gt;ReceiverNumber = (LPWSTR) ( (LPBYTE)FaxReceive-&gt;FileName + sizeof(WCHAR)*(wcslen(FaxReceive-&gt;FileName) + 1));
wcscpy_s(  FaxReceive-&gt;ReceiverNumber, ReceiverNumber );

FaxReceive-&gt;ReceiverName = (LPWSTR) ( (LPBYTE)FaxReceive-&gt;ReceiverNumber+ sizeof(WCHAR)*(wcslen(FaxReceive-&gt;ReceiverNumber) + 1));
wcscpy_s(  FaxReceive-&gt;ReceiverName, ReceiverName );
</pre>
</td>
</tr>
</table></span></div>
<img alt="Filling in the memory that the fax service allocates" src="./images/faxover.png"/>
The FSP can reformat the <b>ReceiverName</b> and <b>ReceiverNumber</b> members and transmit the reformatted data to the remote sending device as the called subscriber identifier (CSI) to comply with the recommendation of the standards body of the International Telecommunication Union (ITU) from Study Group 8 (SG8). For more information, see the <b>RoutingInfo</b> and <b>CSI</b> members of the <a href="https://msdn.microsoft.com/b5d024c2-36f9-4f70-abab-3824f3612089">FAX_DEV_STATUS</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/b5d024c2-36f9-4f70-abab-3824f3612089">FAX_DEV_STATUS</a>



<a href="https://msdn.microsoft.com/4c823cde-c37b-4078-8a83-e58176f80392">Fax Service Provider Structures</a>



<a href="https://msdn.microsoft.com/3f37c113-2971-4092-8753-b0d30b8ce6c1">FaxDevReceive</a>



<a href="https://msdn.microsoft.com/a8788e8a-e97c-4082-8e89-b6f4a7568d3a">Using the Fax Service Provider API</a>
 

 

