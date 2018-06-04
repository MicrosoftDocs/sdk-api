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

# IFsiFileItem2::get_IsRealTime


## -description


Retrieves the property value that specifies if a file item in the file system image is a 'Real-Time' or standard file.


## -parameters




### -param pVal [out]

Pointer to a value that indicates if the Real-Time attribute of the file is set in the file system image.  A value of <b>VARIANT_TRUE</b>indicates the attribute is set; otherwise, <b>VARIANT_FALSE</b>.


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
<dt><b>IMAPI_E_PROPERTY_NOT_ACCESSIBLE</b></dt>
<dt>Value: 0xC0AAB160L</dt>
</dl>
</td>
<td width="60%">
Property '<i>%1!ls!</i>' is not accessible.

</td>
</tr>
</table>
 




## -remarks



If this method is invoked for a file item representing a named stream, this method returns error code <b>IMAPI_E_PROPERTY_NOT_ACCESSIBLE</b> as
named streams do not have the Real-Time attribute.

The user must enable UDF and set the UDF revision to 2.01 or higher to support Real-Time files.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/f35d1cd9-8a04-4c12-9af3-38f2c44b8c06">IFsiFileItem2</a>
 

 

