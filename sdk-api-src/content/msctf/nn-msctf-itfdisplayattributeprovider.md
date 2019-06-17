---
UID: NN:msctf.ITfDisplayAttributeProvider
title: ITfDisplayAttributeProvider (msctf.h)
author: windows-sdk-content
description: The ITfDisplayAttributeProvider interface is implemented by a text service and is used by the TSF manager to enumerate and obtain individual display attribute information objects.
old-location: tsf\itfdisplayattributeprovider.htm
tech.root: TSF
ms.assetid: c0346d5e-d4a2-4c72-90be-de5ff1681acd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfDisplayAttributeProvider, ITfDisplayAttributeProvider interface [Text Services Framework], ITfDisplayAttributeProvider interface [Text Services Framework],described, _tsf_itfdisplayattributeprovider_ref, msctf/ITfDisplayAttributeProvider, tsf.itfdisplayattributeprovider
ms.topic: interface
f1_keywords: ["msctf/ITfDisplayAttributeProvider"]
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
req.dll: Imjpcic.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imjpcic.dll
api_name:
 - ITfDisplayAttributeProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfDisplayAttributeProvider interface


## -description


The <b>ITfDisplayAttributeProvider</b> interface is implemented by a text service and is used by the TSF manager to enumerate and obtain individual display attribute information objects.

The TSF manager obtains an instance of this interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with the class identifier passed to <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-registercategory">ITfCategoryMgr::RegisterCategory</a> with GUID_TFCAT_DISPLAYATTRIBUTEPROVIDER and IID_ITfDisplayAttributeProvider. For more information, see <a href="https://docs.microsoft.com/windows/desktop/TSF/providing-display-attributes">Providing Display Attributes</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfDisplayAttributeProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfDisplayAttributeProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfDisplayAttributeProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo">EnumDisplayAttributeInfo</a>
</td>
<td align="left" width="63%">
Obtains an enumerator that contains all display attribute info objects supported by the display attribute provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo">GetDisplayAttributeInfo</a>
</td>
<td align="left" width="63%">
Obtains a display attribute provider object for a particular display attribute.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-registercategory">ITfCategoryMgr::RegisterCategory
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/TSF/providing-display-attributes">Providing Display Attributes</a>
 

 

