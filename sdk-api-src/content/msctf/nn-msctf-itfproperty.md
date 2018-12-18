---
UID: NN:msctf.ITfProperty
title: ITfProperty
author: windows-sdk-content
description: The ITfProperty interface is implemented by the TSF manager and used by a client (application or text service) to modify a property value.
old-location: tsf\itfproperty.htm
tech.root: TSF
ms.assetid: 72bd92f9-d82e-4994-82ad-0989e987903b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfProperty, ITfProperty interface [Text Services Framework], ITfProperty interface [Text Services Framework],described, _tsf_itfproperty_ref, msctf/ITfProperty, tsf.itfproperty
ms.topic: interface
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
 - ITfProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfProperty interface


## -description


The <b>ITfProperty</b> interface is implemented by the TSF manager and used by a client (application or text service) to modify a property value.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfProperty</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbfbbe0d-bea7-4c46-8b9c-6b607a761f48">Clear</a>
</td>
<td align="left" width="63%">
Empties the property value over the specified range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08e9c9c1-768b-406c-96ae-e0776b59344d">FindRange</a>
</td>
<td align="left" width="63%">
Obtains a range that covers the text that contains a non-empty value for the property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72064f9f-311e-4d7b-9ead-4fe2b7f528a8">SetValue</a>
</td>
<td align="left" width="63%">
Sets the value of the property for a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/146af429-54a8-41b6-b44e-b5d35f933435">SetValueStore</a>
</td>
<td align="left" width="63%">
Sets the value of the property for a range of text using a property store object.

</td>
</tr>
</table> 


## -remarks



An instance of this interface is obtained in various ways, such as <a href="https://msdn.microsoft.com/e5d76443-f767-47fb-be3a-8cbac224d299">ITfContext::GetProperty</a> or <a href="https://msdn.microsoft.com/a8357166-bfc3-4740-a5b9-91c6c1825ab9">IEnumTfProperties::Next</a>.




## -see-also




<a href="https://msdn.microsoft.com/a8357166-bfc3-4740-a5b9-91c6c1825ab9">IEnumTfProperties::Next
      </a>



<a href="https://msdn.microsoft.com/e5d76443-f767-47fb-be3a-8cbac224d299">ITfContext::GetProperty
      </a>



<a href="https://msdn.microsoft.com/f4021a3d-6b86-469f-8943-770e7ef0cf99">ITfReadOnlyProperty
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

