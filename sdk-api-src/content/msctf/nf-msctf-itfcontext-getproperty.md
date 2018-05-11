---
UID: NF:msctf.ITfContext.GetProperty
title: ITfContext::GetProperty
author: windows-driver-content
description: ITfContext::GetProperty method
old-location: tsf\itfcontext_getproperty.htm
old-project: TSF
ms.assetid: e5d76443-f767-47fb-be3a-8cbac224d299
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetProperty, GetProperty method [Text Services Framework], GetProperty method [Text Services Framework],ITfContext interface, ITfContext interface [Text Services Framework],GetProperty method, ITfContext.GetProperty, ITfContext::GetProperty, _tsf_itfcontext_getproperty_ref, msctf/ITfContext::GetProperty, tsf.itfcontext_getproperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfContext.GetProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfContext::GetProperty


## -description




## -parameters




### -param guidProp [in]

Specifies the property identifier. This can be a custom identifier or one of the <a href="https://msdn.microsoft.com/d88f2eba-4c98-4b32-96e1-cd019fe0f7ad">predefined property identifiers</a>.


### -param ppProp [out]

Pointer to an <a href="https://msdn.microsoft.com/72bd92f9-d82e-4994-82ad-0989e987903b">ITfProperty</a> interface pointer that receives the property object.


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
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context is not on a document stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

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



An application or text service can define unique properties identified by a GUID. Properties are stored as VARIANT data, so the caller must recognize the format and meaning of unique properties to be able to use them.




## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a>



<a href="https://msdn.microsoft.com/72bd92f9-d82e-4994-82ad-0989e987903b">
        ITfProperty
      </a>



<a href="https://msdn.microsoft.com/d88f2eba-4c98-4b32-96e1-cd019fe0f7ad">Predefined Properties
      </a>
 

 

