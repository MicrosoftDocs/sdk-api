---
UID: NF:wmcodecdsp.IToc.SetDescription
title: IToc::SetDescription
author: windows-sdk-content
description: The SetDescription method associates a description with the table of contents.
old-location: mf\itoc_setdescription.htm
tech.root: medfound
ms.assetid: 718eb8bd-fdf9-434d-b859-3a38cb8fabee
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IToc interface [Media Foundation],SetDescription method, IToc.SetDescription, IToc::SetDescription, SetDescription, SetDescription method [Media Foundation], SetDescription method [Media Foundation],IToc interface, codecapi.itoc_setdescription, mf.itoc_setdescription, wmcodecdsp/IToc::SetDescription
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Wmvdspa.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmvdspa.dll
api_name:
 - IToc.SetDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IToc::SetDescription


## -description


The <b>SetDescription</b> method associates a description with the table of contents.


## -parameters




### -param pwszDescription [in]

Pointer to a NULL-terminated, wide-character string that contains the description.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



You can use this method to associate any description with the table of contents. TOC parser does not inspect or interpret the description.




## -see-also




<a href="https://msdn.microsoft.com/660d4da9-ddbc-466c-ab1a-7e60ecf61473">GetDescription</a>



<a href="https://msdn.microsoft.com/b12d38c7-b80e-4ca8-9ac5-a116100911d0">IToc</a>
 

 

