---
UID: NF:msctf.ITfContextOwnerServices.ForceLoadProperty
title: ITfContextOwnerServices::ForceLoadProperty
author: windows-sdk-content
description: ITfContextOwnerServices::ForceLoadProperty method
old-location: tsf\itfcontextownerservices_forceloadproperty.htm
tech.root: TSF
ms.assetid: 7f77d82f-e048-463f-bf0d-15bf1daaddb6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ForceLoadProperty, ForceLoadProperty method [Text Services Framework], ForceLoadProperty method [Text Services Framework],ITfContextOwnerServices interface, ITfContextOwnerServices interface [Text Services Framework],ForceLoadProperty method, ITfContextOwnerServices.ForceLoadProperty, ITfContextOwnerServices::ForceLoadProperty, _tsf_itfcontextownerservices_forceloadproperty_ref, msctf/ITfContextOwnerServices::ForceLoadProperty, tsf.itfcontextownerservices_forceloadproperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfContextOwnerServices.ForceLoadProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
- apiref
: 
- COM
: 
- msctf.h
: 
- ITfContextOwnerServices.ForceLoadProperty
: 
---

# ITfContextOwnerServices::ForceLoadProperty


## -description




## -parameters




### -param pProp [in]

Pointer to an <a href="https://msdn.microsoft.com/72bd92f9-d82e-4994-82ad-0989e987903b">ITfProperty</a> object that specifies the property to load.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation error occurred.

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
</table>
 




## -remarks



The application must be able to grant a synchronous read-only lock before calling this method.




## -see-also




<a href="https://msdn.microsoft.com/fb77bd6a-ae34-4e21-8f09-fc8c6a1ade86">ITfContextOwnerServices</a>



<a href="https://msdn.microsoft.com/b02ffedf-83c5-48ff-8116-801aaec6dc71">ITfContextOwnerServices::Unserialize
      </a>



<a href="https://msdn.microsoft.com/72bd92f9-d82e-4994-82ad-0989e987903b">ITfProperty
      </a>
 

 

