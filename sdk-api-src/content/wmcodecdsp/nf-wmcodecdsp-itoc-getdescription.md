---
UID: NF:wmcodecdsp.IToc.GetDescription
title: IToc::GetDescription
author: windows-sdk-content
description: The GetDescription method retrieves the description, set by a previous call to SetDescription, of the table of contents.
old-location: mf\itoc_getdescription.htm
tech.root: medfound
ms.assetid: 660d4da9-ddbc-466c-ab1a-7e60ecf61473
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetDescription, GetDescription method [Media Foundation], GetDescription method [Media Foundation],IToc interface, IToc interface [Media Foundation],GetDescription method, IToc.GetDescription, IToc::GetDescription, codecapi.itoc_getdescription, mf.itoc_getdescription, wmcodecdsp/IToc::GetDescription
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
 - IToc.GetDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IToc::GetDescription


## -description


The <b>GetDescription</b> method retrieves the description, set by a previous call to <a href="https://msdn.microsoft.com/718eb8bd-fdf9-434d-b859-3a38cb8fabee">SetDescription</a>, of the table of contents.


## -parameters




### -param pwDescriptionSize [in, out]

If <i>pwszDescription</i> is <b>NULL</b>, this is an output parameter that receives the size, in wide characters, of the buffer required to receive the description. If <i>pwszDescription</i> is not <b>NULL</b>, this is an input parameter that specifies the size, in wide characters, of the caller-allocated buffer pointed to by <i>pwszDescription</i>.


### -param pwszDescription [out]

<b>NULL</b>, or a pointer to a caller-allocated buffer that, on successful completion, receives the description. The description is null-terminated.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The method returns this error code if <i>pwszDescription</i> is not <b>NULL</b> and the description, including its NULL terminator, is larger than the size specified by <i>pwDescriptionSize</i>. In that case, <i>pwDescriptionSize</i> serves as an output parameter and receives the size of the required buffer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b12d38c7-b80e-4ca8-9ac5-a116100911d0">IToc</a>
 

 

