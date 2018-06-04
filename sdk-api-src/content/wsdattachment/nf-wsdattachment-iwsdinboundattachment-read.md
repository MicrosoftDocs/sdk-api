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

# IWSDInboundAttachment::Read


## -description


Retrieves attachment data from a message sent by a remote host.


## -parameters




### -param pBuffer [out]

Pointer to a buffer receiving the data read from the attachment stream. The application program is responsible for allocating and freeing this data buffer.


### -param dwBytesToRead [in]

Size of the <i>pBuffer</i> input buffer, in bytes.


### -param pdwNumberOfBytesRead






#### - pdwNumberofBytesRead [out]

Pointer to a <b>DWORD</b> containing the number of bytes of data read from the attachment stream into the <i>pBuffer</i> input buffer.


## -returns



Possible return values include, but are not limited to, the following:

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The end of the attachment stream has been reached.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pBuffer</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pdwNumberofBytesRead</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The <b>Read</b> method allows an application to receive arbitrary data from a remote host in a MIME-encapsulated message attachment. WSDAPI will provide an object implementing this interface when an attachment stream is received as part of a message. The call to <b>Read</b> opens the inbound attachment stream and transfers the attachment data to the application's buffer. If <b>Read</b> returns S_OK or S_FALSE, <i>pdwNumberofBytesRead</i> is set to the number of bytes read, which may be less than the size of the buffer. The <b>Read</b> call may block on network traffic.




## -see-also




<a href="https://msdn.microsoft.com/1bacbf20-2eb2-4aa1-ba37-e14dc0d955b0">IWSDInboundAttachment</a>
 

 

