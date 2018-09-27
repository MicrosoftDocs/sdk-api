---
UID: NF:ocidl.IFont.put_Name
title: IFont::put_Name
author: windows-sdk-content
description: Specifies a new name for the font family.
old-location: com\ifont_put_name.htm
tech.root: com
ms.assetid: 3593d5c9-e2b7-4d85-b8f7-94f01a901030
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFont interface [COM],put_Name method, IFont.put_Name, IFont::put_Name, _ctrl_ifont_put_name, com.ifont_put_name, ocidl/IFont::put_Name, put_Name, put_Name method [COM], put_Name method [COM],IFont interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - OCIdl.h
api_name:
 - IFont.put_Name
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFont::put_Name


## -description


Specifies a new name for the font family.


## -parameters




### -param name [in]

The new name of the font family. This value is both allocated and freed by 
      the caller.


## -returns



The method supports the standard return value <b>E_UNEXPECTED</b>, as well as the 
      following values.

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
The name was changed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in the <i>name</i> parameter is not valid. For example, it may be 
        <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The string value is caller allocated and the caller is responsible for freeing it after this call 
    returns.




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/04ce50a6-b833-4476-91a9-0d1ca7296314">IFont::get_Name</a>
 

 

