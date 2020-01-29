---
UID: NL:vswriter.IVssComponentEx2
title: IVssComponentEx2 (vswriter.h)
description: Defines additional methods for reporting and retrieving component-level writer errors.
old-location: base\ivsscomponentex2.htm
tech.root: VSS
ms.assetid: f40705bf-46a9-464d-a545-1d68d89876c2
ms.date: 12/05/2018
ms.keywords: IVssComponentEx2, IVssComponentEx2 interface, IVssComponentEx2 interface,described, base.ivsscomponentex2, vswriter/IVssComponentEx2
f1_keywords:
- vswriter/IVssComponentEx2
dev_langs:
- c++
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- VssApi.lib
- VssApi.dll
api_name:
- IVssComponentEx2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssComponentEx2 class


## -description


Defines additional methods for reporting and retrieving component-level writer errors.

The <b>IVssComponentEx2</b> interface is a C++ (not COM) interface.

To obtain an instance of the <b>IVssComponentEx2</b> 
   interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of the 
   <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a> interface and pass 
   the <b>IID_IVssComponentEx2</b> constant as the interface identifier (IID) parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssComponentEx2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-ivsscomponentex">IVssComponentEx</a> and <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>. <b>IVssComponentEx2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssComponentEx2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex2-getfailure">GetFailure</a>
</td>
<td align="left" width="63%">
VSS requesters call this method to retrieve component-level errors reported by writers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex2-setfailure">SetFailure</a>
</td>
<td align="left" width="63%">
VSS writers call this method to report errors at the component level.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-ivsscomponentex">IVssComponentEx</a>
 

 

