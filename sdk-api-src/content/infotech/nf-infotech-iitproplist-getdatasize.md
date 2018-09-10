---
UID: NF:infotech.IITPropList.GetDataSize
title: IITPropList::GetDataSize
author: windows-sdk-content
description: Returns the number of bytes needed to save the property data.
old-location: htmlhelp\iitproplist_getdatasize.htm
tech.root: htmlhelp
ms.assetid: 83d9fa7b-d814-4293-93b9-9454c01c1503
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetDataSize, GetDataSize method [HTML Help Workshop], GetDataSize method [HTML Help Workshop],IITPropList interface, IITPropList interface [HTML Help Workshop],GetDataSize method, IITPropList.GetDataSize, IITPropList::GetDataSize, htmlhelp.iitproplist_getdatasize, infotech/IITPropList::GetDataSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: infotech.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Infotech.h
api_name:
 - IITPropList.GetDataSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IITPropList::GetDataSize


## -description


Returns the number of bytes needed to save the property data. 


## -parameters




### -param lpvHeader [in]

Pointer to a buffer containing the header. 


### -param dwHdrSize [in]

Size of the header buffer. 


### -param dwDataSize [out, ref]

Size in bytes. 


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
The size was successfully returned. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvHeader</i> parameter is NULL, or <i>dwHdrSize</i> is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BADVALUE</b></dt>
</dl>
</td>
<td width="60%">
Invalid header buffer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/09200749-bd1d-4266-895e-29e21525bac2">IITPropList</a>



<a href="https://msdn.microsoft.com/73206149-cbc3-475d-8dc8-bb7547f41173">IITPropList::GetHeaderSize</a>
 

 

