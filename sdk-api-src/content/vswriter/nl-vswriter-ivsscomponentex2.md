---
UID: NL:vswriter.IVssComponentEx2
title: IVssComponentEx2
author: windows-sdk-content
description: Defines additional methods for reporting and retrieving component-level writer errors.
old-location: base\ivsscomponentex2.htm
old-project: vss
ms.assetid: f40705bf-46a9-464d-a545-1d68d89876c2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IVssComponentEx2, IVssComponentEx2 interface, IVssComponentEx2 interface,described, base.ivsscomponentex2, vswriter/IVssComponentEx2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
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
tech.root: 
req.typenames: VSS_WRITERRESTORE_ENUM
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
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssComponentEx2 class


## -description


Defines additional methods for reporting and retrieving component-level writer errors.

The <b>IVssComponentEx2</b> interface is a C++ (not COM) interface.

To obtain an instance of the <b>IVssComponentEx2</b> 
   interface, call the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> method of the 
   <a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a> interface and pass 
   the <b>IID_IVssComponentEx2</b> constant as the interface identifier (IID) parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssComponentEx2</b> interface inherits from <a href="https://msdn.microsoft.com/b11f65b0-2de2-478b-88b6-4696a8da2419">IVssComponentEx</a> and <a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>. <b>IVssComponentEx2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a5d739d3-9169-4b25-a590-35703e77dacc">GetFailure</a>
</td>
<td align="left" width="63%">
VSS requesters call this method to retrieve component-level errors reported by writers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9fd728a-b205-4cfa-8e9e-e0a0d385f5a1">SetFailure</a>
</td>
<td align="left" width="63%">
VSS writers call this method to report errors at the component level.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>



<a href="https://msdn.microsoft.com/b11f65b0-2de2-478b-88b6-4696a8da2419">IVssComponentEx</a>
 

 

