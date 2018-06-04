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

# IMetaDataImport2::GetPEKind


## -description


Gets a value identifying the nature of the code in the portable executable (PE) file, typically a DLL or EXE file, that is defined in the current metadata scope.


## -parameters




### -param pdwPEKind [out]

 A pointer to a value of the <a href="http://msdn.microsoft.com/en-us/library/ms230275.aspx">CorPEKind</a> enumeration that describes the PE file.


### -param pdwMAchine [out]

A pointer to a value that identifies the architecture of the machine. See the next section for possible values.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The value referenced by the <i>pdwMachine</i> parameter can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Machine architecture</th>
</tr>
<tr>
<td>
IMAGE_FILE_MACHINE_I386



0x014C


</td>
<td>x86
</td>
</tr>
<tr>
<td>
IMAGE_FILE_MACHINE_IA64



0x0200


</td>
<td>Intel IPF
</td>
</tr>
<tr>
<td>
IMAGE_FILE_MACHINE_AMD64



0x8664


</td>
<td>x64
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/32c462e0-d4b8-44db-b24b-c86b46be85bf">IMetaDataImport2</a>
 

 

