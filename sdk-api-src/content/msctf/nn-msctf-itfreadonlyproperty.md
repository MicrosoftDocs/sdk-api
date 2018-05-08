---
UID: NN:msctf.ITfReadOnlyProperty
title: ITfReadOnlyProperty
author: windows-driver-content
description: The ITfReadOnlyProperty interface is implemented by the TSF manager and used by an application or text service to obtain property data.
old-location: tsf\itfreadonlyproperty.htm
old-project: TSF
ms.assetid: f4021a3d-6b86-469f-8943-770e7ef0cf99
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfReadOnlyProperty, ITfReadOnlyProperty interface [Text Services Framework], ITfReadOnlyProperty interface [Text Services Framework],described, _tsf_itfreadonlyproperty_ref, msctf/ITfReadOnlyProperty, tsf.itfreadonlyproperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	ITfReadOnlyProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfReadOnlyProperty interface


## -description


The <b>ITfReadOnlyProperty</b> interface is implemented by the TSF manager and used by an application or text service to obtain property data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfReadOnlyProperty</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfReadOnlyProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfReadOnlyProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/201c518b-f06f-4c4f-aa56-f8d21f477814">EnumRanges</a>
</td>
<td align="left" width="63%">
Obtains an enumeration of ranges that contain unique values of the property within the given range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff545736">GetContext</a>
</td>
<td align="left" width="63%">
Obtains the context object for the property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Obtains the property identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597624">GetValue</a>
</td>
<td align="left" width="63%">
Obtains the value of the property for a range of text.

</td>
</tr>
</table> 


## -remarks



An instance of this interface is obtained by using <a href="https://msdn.microsoft.com/5c04ff8e-5686-4802-b312-71dddaf0155e">ITfContext::GetAppProperty</a> or <a href="https://msdn.microsoft.com/e283a45d-b585-4a26-89db-7ed706f0f593">ITfContext::TrackProperties</a>.




## -see-also




<a href="https://msdn.microsoft.com/5c04ff8e-5686-4802-b312-71dddaf0155e">ITfContext::GetAppProperty
      </a>



<a href="https://msdn.microsoft.com/e283a45d-b585-4a26-89db-7ed706f0f593">
        ITfContext::TrackProperties
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

