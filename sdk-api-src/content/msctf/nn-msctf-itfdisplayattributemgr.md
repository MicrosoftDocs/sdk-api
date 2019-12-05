---
UID: NN:msctf.ITfDisplayAttributeMgr
title: ITfDisplayAttributeMgr (msctf.h)
description: The ITfDisplayAttributeMgr interface is implemented by the TSF manager and used by an application to obtain and enumerate display attributes. Individual display attributes are accessed through the ITfDisplayAttributeInfo interface.
old-location: tsf\itfdisplayattributemgr.htm
tech.root: TSF
ms.assetid: 4a1f9a13-54a1-4294-9635-80eef8bcd8d5
ms.date: 12/05/2018
ms.keywords: ITfDisplayAttributeMgr, ITfDisplayAttributeMgr interface [Text Services Framework], ITfDisplayAttributeMgr interface [Text Services Framework],described, _tsf_itfdisplayattributemgr_ref, msctf/ITfDisplayAttributeMgr, tsf.itfdisplayattributemgr
ms.topic: interface
f1_keywords:
- msctf/ITfDisplayAttributeMgr
dev_langs:
- c++
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
- ITfDisplayAttributeMgr
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfDisplayAttributeMgr interface


## -description


The <b>ITfDisplayAttributeMgr</b> interface is implemented by the TSF manager and used by an application to obtain and enumerate display attributes. Individual display attributes are accessed through the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfdisplayattributeinfo">ITfDisplayAttributeInfo</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfDisplayAttributeMgr</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfDisplayAttributeMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfDisplayAttributeMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo">EnumDisplayAttributeInfo</a>
</td>
<td align="left" width="63%">
Obtains a display attribute enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo">GetDisplayAttributeInfo</a>
</td>
<td align="left" width="63%">
Obtains a display attribute data object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdisplayattributemgr-onupdateinfo">OnUpdateInfo</a>
</td>
<td align="left" width="63%">
Called when a display attribute is changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfdisplayattributeinfo">ITfDisplayAttributeInfo
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

