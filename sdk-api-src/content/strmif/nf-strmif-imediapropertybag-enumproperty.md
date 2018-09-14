---
UID: NF:strmif.IMediaPropertyBag.EnumProperty
title: IMediaPropertyBag::EnumProperty
author: windows-sdk-content
description: The EnumProperty method retrieves a property/value pair.
old-location: dshow\imediapropertybag_enumproperty.htm
tech.root: DirectShow
ms.assetid: 88cd9016-ef6f-467a-9e84-10b2ac578211
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: EnumProperty, EnumProperty method [DirectShow], EnumProperty method [DirectShow],IMediaPropertyBag interface, IMediaPropertyBag interface [DirectShow],EnumProperty method, IMediaPropertyBag.EnumProperty, IMediaPropertyBag::EnumProperty, IMediaPropertyBagEnumProperty, dshow.imediapropertybag_enumproperty, strmif/IMediaPropertyBag::EnumProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaPropertyBag.EnumProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaPropertyBag::EnumProperty


## -description



The <code>EnumProperty</code> method retrieves a property/value pair.




## -parameters




### -param iProperty [in]

Index value of the pair.


### -param pvarPropertyName [in, out]

Pointer to a <b>VARIANT</b> that receives the property's name.


### -param pvarPropertyValue [in, out]

Pointer to a <b>VARIANT</b> that receives the property's value.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following:

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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NO_MORE_ITEMS)</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
</tr>
</table>
 




## -remarks



The name is always a string. Set the variant type of the <i>pvarPropertyName</i> parameter to VT_EMPTY or VT_BSTR before calling this method.

The value can be a string (for INFO chunks) or an array of bytes (for DISP chunks). Set the variant type of the <i>pvarPropertyName</i> parameter to VT_EMPTY, VT_BSTR, or (VT_ARRAY | VT_UI1).




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6f134160-b0aa-44fd-b1b9-938f11349eac">IMediaPropertyBag Interface</a>
 

 

