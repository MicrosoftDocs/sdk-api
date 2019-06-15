---
UID: NN:msctf.ITfDisplayAttributeInfo
title: ITfDisplayAttributeInfo (msctf.h)
author: windows-sdk-content
description: The ITfDisplayAttributeInfo interface is implemented by a text service to provide display attribute data. This interface is used by any component, most often an application, that must determine how text displays.
old-location: tsf\itfdisplayattributeinfo.htm
tech.root: TSF
ms.assetid: 7f590ecf-06e9-42da-ba40-4364296ae594
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfDisplayAttributeInfo, ITfDisplayAttributeInfo interface [Text Services Framework], ITfDisplayAttributeInfo interface [Text Services Framework],described, _tsf_itfdisplayattributeinfo_ref, msctf/ITfDisplayAttributeInfo, tsf.itfdisplayattributeinfo
ms.topic: interface
f1_keywords: ["msctf/ITfDisplayAttributeInfo"]
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
 - ITfDisplayAttributeInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfDisplayAttributeInfo interface


## -description


The <b>ITfDisplayAttributeInfo</b> interface is implemented by a text service to provide display attribute data. This interface is used by any component, most often an application, that must determine how text displays.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfDisplayAttributeInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfDisplayAttributeInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfDisplayAttributeInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdisplayattributeinfo-getattributeinfo">GetAttributeInfo</a>
</td>
<td align="left" width="63%">
Obtains the display attribute data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdisplayattributeinfo-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Obtains the description string of the display attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdisplayattributeinfo-getguid">GetGUID</a>
</td>
<td align="left" width="63%">
Obtains the GUID for the display attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdisplayattributeinfo-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the display attribute data to its default value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdisplayattributeinfo-setattributeinfo">SetAttributeInfo</a>
</td>
<td align="left" width="63%">
Sets the new attribute data.

</td>
</tr>
</table> 


## -remarks



An application obtains an instance of this interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</a> or <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfdisplayattributeinfo-next">IEnumTfDisplayAttributeInfo::Next</a>.

A text service supplies an instance of this interface in its <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfdisplayattributeinfo-next">IEnumTfDisplayAttributeInfo::Next
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo">ITfDisplayAttributeMgr::GetDisplayAttributeInfo
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo">ITfDisplayAttributeProvider::GetDisplayAttributeInfo
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

