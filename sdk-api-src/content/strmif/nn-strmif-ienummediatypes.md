---
UID: NN:strmif.IEnumMediaTypes
title: IEnumMediaTypes
author: windows-sdk-content
description: The IEnumMediaTypes interface enumerates a pin's preferred media types.
old-location: dshow\ienummediatypes.htm
tech.root: DirectShow
ms.assetid: e0021e27-0e08-4d07-9610-08a9b945ae34
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IEnumMediaTypes, IEnumMediaTypes interface [DirectShow], IEnumMediaTypes interface [DirectShow],described, IEnumMediaTypesInterface, dshow.ienummediatypes, strmif/IEnumMediaTypes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IEnumMediaTypes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumMediaTypes interface


## -description


The <b>IEnumMediaTypes</b> interface enumerates a pin's preferred media types. To obtain this interface, call the <a href="https://msdn.microsoft.com/288be4db-5236-40e5-bd92-d95b1bfb86fa">IPin::EnumMediaTypes</a> method on the pin. Filters use this interface when they connect to other filters. Applications can also use it to examine a pin's preferred media types. For more information, see <a href="https://msdn.microsoft.com/04a3dbc8-33c4-4b70-930e-686be2f8301f">Enumerating Objects in a Filter Graph</a>.

This interface implements a standard Component Object Model (COM) collection object. 

If a pin's set of preferred media types changes, some methods on this interface return <b>VFW_E_ENUM_OUT_OF_SYNC</b>. Call the <a href="https://msdn.microsoft.com/d95d4e69-48dc-4ad1-a0e2-c5fea793b7b3">IEnumMediaTypes::Reset</a> method to resynchronize the enumerator.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumMediaTypes</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumMediaTypes</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumMediaTypes</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a81496d-34e5-43d2-aad9-510ab515adc2">Clone</a>
</td>
<td align="left" width="63%">
Makes a copy of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a57fa8e-756b-457c-918a-154fbd085ea3">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of media types.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d95d4e69-48dc-4ad1-a0e2-c5fea793b7b3">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/313628d0-256c-4142-bba5-7cd0c910610c">Skip</a>
</td>
<td align="left" width="63%">
Skips over a specified number of media types.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/7878885f-c285-4744-8eab-445678dcfd49">Enumerating Media Types</a>



<a href="https://msdn.microsoft.com/5efd174f-2eb1-44e6-97e3-b73c7c52fef1">Interfaces</a>
 

 

