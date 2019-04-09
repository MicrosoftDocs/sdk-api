---
UID: NF:amsi.IAmsiStream.Read
title: IAmsiStream::Read (amsi.h)
author: windows-sdk-content
description: Requests a buffer-full of content to be read.
old-location: amsi\iamsistream_read.htm
tech.root: AMSI
ms.assetid: ACE164EF-B49D-4AD5-BC1B-9770AFCD1951
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAmsiStream interface [Antimalware Scan Interface],Read method, IAmsiStream.Read, IAmsiStream::Read, Read, Read method [Antimalware Scan Interface], Read method [Antimalware Scan Interface],IAmsiStream interface, amsi.iamsistream_read, amsi/IAmsiStream::Read
ms.topic: method
req.header: amsi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - COM
api_location:
 - amsi.h
api_name:
 - IAmsiStream.Read
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAmsiStream::Read


## -description


Requests a buffer-full of content to be read.


## -parameters




### -param position [in]

The zero-based index into the content at which the read is to begin.


### -param size [in]

The number of bytes to read from the content.


### -param buffer [out]

Buffer into which the content is to be read.


### -param readSize [out]

The number of bytes read into <i>buffer</i>.


## -returns



This method can return one of these values.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more argument is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOT_VALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The object is not initialized.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/409CE6BF-57A5-454E-91F9-3D66FE7E323F">IAmsiStream</a>
 

 

