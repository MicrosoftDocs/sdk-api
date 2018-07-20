---
UID: NN:msctf.ITfDisplayAttributeMgr
title: ITfDisplayAttributeMgr
author: windows-sdk-content
description: The ITfDisplayAttributeMgr interface is implemented by the TSF manager and used by an application to obtain and enumerate display attributes. Individual display attributes are accessed through the ITfDisplayAttributeInfo interface.
old-location: tsf\itfdisplayattributemgr.htm
old-project: TSF
ms.assetid: 4a1f9a13-54a1-4294-9635-80eef8bcd8d5
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfDisplayAttributeMgr, ITfDisplayAttributeMgr interface [Text Services Framework], ITfDisplayAttributeMgr interface [Text Services Framework],described, _tsf_itfdisplayattributemgr_ref, msctf/ITfDisplayAttributeMgr, tsf.itfdisplayattributemgr
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfDisplayAttributeMgr
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfDisplayAttributeMgr interface


## -description


The <b>ITfDisplayAttributeMgr</b> interface is implemented by the TSF manager and used by an application to obtain and enumerate display attributes. Individual display attributes are accessed through the <a href="https://msdn.microsoft.com/7f590ecf-06e9-42da-ba40-4364296ae594">ITfDisplayAttributeInfo</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfDisplayAttributeMgr</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfDisplayAttributeMgr</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ea0cb5b1-46a3-43c6-a109-1972d3fcbc18">EnumDisplayAttributeInfo</a>
</td>
<td align="left" width="63%">
Obtains a display attribute enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41bc183f-013f-4e68-bb72-d9a30d5ea48e">GetDisplayAttributeInfo</a>
</td>
<td align="left" width="63%">
Obtains a display attribute data object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f906a19-16b8-47c1-adca-10d6da0cc7dd">OnUpdateInfo</a>
</td>
<td align="left" width="63%">
Called when a display attribute is changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/7f590ecf-06e9-42da-ba40-4364296ae594">ITfDisplayAttributeInfo
      </a>



<a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

