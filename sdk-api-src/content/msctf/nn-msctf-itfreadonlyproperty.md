---
UID: NN:msctf.ITfReadOnlyProperty
title: ITfReadOnlyProperty (msctf.h)
author: windows-sdk-content
description: The ITfReadOnlyProperty interface is implemented by the TSF manager and used by an application or text service to obtain property data.
old-location: tsf\itfreadonlyproperty.htm
tech.root: TSF
ms.assetid: f4021a3d-6b86-469f-8943-770e7ef0cf99
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfReadOnlyProperty, ITfReadOnlyProperty interface [Text Services Framework], ITfReadOnlyProperty interface [Text Services Framework],described, _tsf_itfreadonlyproperty_ref, msctf/ITfReadOnlyProperty, tsf.itfreadonlyproperty
ms.topic: interface
f1_keywords: 
 - "msctf/ITfReadOnlyProperty"
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
 - ITfReadOnlyProperty
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfReadOnlyProperty interface


## -description


The <b>ITfReadOnlyProperty</b> interface is implemented by the TSF manager and used by an application or text service to obtain property data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfReadOnlyProperty</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfReadOnlyProperty</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges">EnumRanges</a>
</td>
<td align="left" width="63%">
Obtains an enumeration of ranges that contain unique values of the property within the given range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getcontext">GetContext</a>
</td>
<td align="left" width="63%">
Obtains the context object for the property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-gettype">GetType</a>
</td>
<td align="left" width="63%">
Obtains the property identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Obtains the value of the property for a range of text.

</td>
</tr>
</table> 


## -remarks



An instance of this interface is obtained by using <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty">ITfContext::GetAppProperty</a> or <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontext-trackproperties">ITfContext::TrackProperties</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty">ITfContext::GetAppProperty
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontext-trackproperties">ITfContext::TrackProperties
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

