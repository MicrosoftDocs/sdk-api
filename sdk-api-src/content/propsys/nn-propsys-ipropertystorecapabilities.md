---
UID: NN:propsys.IPropertyStoreCapabilities
title: IPropertyStoreCapabilities (propsys.h)
author: windows-sdk-content
description: Exposes a method that determines whether a property can be edited in the UI by the user.
old-location: properties\IPropertyStoreCapabilities.htm
tech.root: properties
ms.assetid: b4e51201-47af-449f-9050-aec3207320f5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPropertyStoreCapabilities, IPropertyStoreCapabilities interface [Windows Properties], IPropertyStoreCapabilities interface [Windows Properties],described, _shell_IPropertyStoreCapabilities, properties.IPropertyStoreCapabilities, propsys/IPropertyStoreCapabilities, shell.IPropertyStoreCapabilities
ms.topic: interface
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - Propsys.h
api_name:
 - IPropertyStoreCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyStoreCapabilities interface


## -description


Exposes a method that determines whether a property can be edited in the UI by the user.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyStoreCapabilities</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPropertyStoreCapabilities</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyStoreCapabilities</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761454(v=VS.85).aspx">IsPropertyWritable</a>
</td>
<td align="left" width="63%">
Queries whether the property handler allows a specific property to be edited in the UI by the user.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Property handlers implement this interface to disable a user's ability to edit specific properties. These properties are typically editable in the UI, but are not supported for writing by the property handler. For example, the property System.Author is typically editable. If a property handler author created a file type that exposed <a href="https://msdn.microsoft.com/en-us/library/Bb760652(v=VS.85).aspx">System.Author</a> for reading, but could not support writing this property back, the handler author could return S_FALSE from <a href="https://msdn.microsoft.com/en-us/library/Bb761454(v=VS.85).aspx">IPropertyStoreCapabilities::IsPropertyWritable</a> for System.Author.

The Shell user interfaces that allow property editing, such as the <b>Details Pane</b> and <b>Details Tab</b> of the Properties dialog, call this method as part of determining whether to allow editing of a specific property. This allows the Shell property editing UI to disable controls rather than showing errors when the property handler fails to set or commit the property value. 



