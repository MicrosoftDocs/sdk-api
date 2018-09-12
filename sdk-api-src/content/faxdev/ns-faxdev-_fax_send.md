---
UID: NS:faxdev._FAX_SEND
title: "_FAX_SEND"
author: windows-sdk-content
description: The FAX_SEND structure contains information about an outbound fax document.
old-location: fax\_mfax_fax_send_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_8ueq.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: "*PFAX_SEND, FAX_SEND, FAX_SEND structure [Fax Service], PFAX_SEND, PFAX_SEND structure pointer [Fax Service], _FAX_SEND, _mfax_fax_send_str, fax._mfax_fax_send_str, faxdev/FAX_SEND, faxdev/PFAX_SEND"
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
 - FAX_SEND
product: Windows
targetos: Windows
req.typenames: FAX_SEND, *PFAX_SEND
req.redist: 
---

# _FAX_SEND structure


## -description


The <b>FAX_SEND</b> structure contains information about an outbound fax document. The structure contains the name of the file that holds the fax data stream, the name and telephone number of the calling device, and the name and telephone number of the receiving device.


## -struct-fields




### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies, in bytes, the size of the <b>FAX_SEND</b> structure. Before calling the <a href="https://msdn.microsoft.com/9ec25812-658f-4d64-85c4-8ab66be5d93e">FaxDevSend</a> function, the fax service sets this member to <b>sizeof</b>(<b>FAX_SEND</b>). 


### -field FileName

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode character string that specifies the full path to the file that contains the data stream for an outbound fax document. The data stream is a TIFF Class F file. For more information, see <a href="https://msdn.microsoft.com/d7840c10-6059-40ed-9040-50eefefc7349">Fax Image Format</a>.


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

 




#### - Reserved[3]

Type: <b>DWORD</b>

This member is reserved  by Microsoft. It must be set to zero.


## -remarks



The FSP can reformat the <b>CallerName</b> and <b>CallerNumber</b> members. The FSP can then transmit the reformatted data to the remote sending device as the called subscriber identifier (CSI) to comply with the recommendation of the standards body of the International Telecommunication Union (ITU) from Study Group 8 (SG8). For more information, see the <b>RoutingInfo</b> and <b>CSI</b> members of the <a href="https://msdn.microsoft.com/b5d024c2-36f9-4f70-abab-3824f3612089">FAX_DEV_STATUS</a> structure.

The FSP can also use the reformatted data to add a brand to the fax transmission.




## -see-also




<a href="https://msdn.microsoft.com/b5d024c2-36f9-4f70-abab-3824f3612089">FAX_DEV_STATUS</a>



<a href="https://msdn.microsoft.com/4c823cde-c37b-4078-8a83-e58176f80392">Fax Service Provider Structures</a>



<a href="https://msdn.microsoft.com/9ec25812-658f-4d64-85c4-8ab66be5d93e">FaxDevSend</a>



<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/a8788e8a-e97c-4082-8e89-b6f4a7568d3a">Using the Fax Service Provider API</a>
 

 

