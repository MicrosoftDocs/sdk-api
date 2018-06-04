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

# GetPreferredPacketDescription function


## -description



Retrieves a packet description that contains the packet properties the recognizer uses.




## -parameters




### -param hrec

Handle to the recognizer.


### -param pPacketDescription

Describes the content of the packets the recognizer uses. For more information, see the <a href="https://msdn.microsoft.com/6823f2c6-2c99-4b9a-8208-041fc1f7bf82">PACKET_DESCRIPTION</a> structure.

To retrieve the packet description, initialize the packet description with zeroes and call the <b>GetPreferredPacketDescription</b> function. The function populates the property and button counts, which you use to allocate space for the pPacketProperties and pguidButtons members of the <a href="https://msdn.microsoft.com/6823f2c6-2c99-4b9a-8208-041fc1f7bf82">PACKET_DESCRIPTION</a> structure. Call the function again to populate the rest of the packet description.

The pguidButtons member of the <a href="https://msdn.microsoft.com/6823f2c6-2c99-4b9a-8208-041fc1f7bf82">PACKET_DESCRIPTION</a> structure may be zero when <b>GetPreferredPacketDescription</b> returns. This means the packets have no button data, so this member does not have any pguidButtons allocated. In this case, the calling function should leave the pointer <b>NULL</b>.


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pPacketDescription</i> buffer is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
</table>
 




## -remarks



Typically, recognizers use the (x, y) coordinate properties and ignore the others. If you save the ink to a file for recognition at a later time, use the preferred packet description to only save those properties that the recognizer uses.




## -see-also




<a href="https://msdn.microsoft.com/1db3dbef-41bf-4b00-8e6c-07c7c414e595">AddStroke Function</a>



<a href="https://msdn.microsoft.com/6823f2c6-2c99-4b9a-8208-041fc1f7bf82">PACKET_DESCRIPTION Structure</a>
 

 

