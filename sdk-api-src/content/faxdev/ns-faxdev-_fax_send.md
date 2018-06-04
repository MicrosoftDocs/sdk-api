---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

