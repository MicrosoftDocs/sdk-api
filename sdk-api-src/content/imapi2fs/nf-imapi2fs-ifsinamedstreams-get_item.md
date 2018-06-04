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

# IFsiNamedStreams::get_Item


## -description


Retrieves a  single named stream associated with a file in the file system image.


## -parameters




### -param index [in]

This value indicates the position of the named stream within the  collection.
	The index number is zero-based, i.e. the first item is at location 0 of the collection.


### -param item [out, optional]

Pointer to a pointer to an <a href="https://msdn.microsoft.com/f35d1cd9-8a04-4c12-9af3-38f2c44b8c06">IFsiFileItem2</a> object representing the named stream at the  position specified by <i>index</i>. This parameter is set to <b>NULL</b> if the specified index is not within the collection boundary.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
<dt>Value: 0x80004003</dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_INVALID_PARAM</b></dt>
<dt>Value: 0xC0AAB101</dt>
</dl>
</td>
<td width="60%">
The value specified for parameter '<i>%1!ls!</i>' is invalid.

</td>
</tr>
</table>
 




## -remarks



If the index number is negative or out of range, this method returns the <b>IMAPI_E_INVALID_PARAM</b>.

To fetch an <b>IEnumVARIANT</b> enumerator for all named streams associated with a file, use the <a href="https://msdn.microsoft.com/ea1a14fe-91f0-4710-9d15-66a4c415f541">IFsiNamedStreams::get__NewEnum</a> method.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/383a83e4-5dc2-459a-a58f-b6ce7a656348">IFsiNamedStreams</a>
 

 

