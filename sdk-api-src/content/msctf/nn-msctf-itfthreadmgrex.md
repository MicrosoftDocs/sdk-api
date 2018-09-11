---
UID: NN:msctf.ITfThreadMgrEx
title: ITfThreadMgrEx
author: windows-sdk-content
description: The ITfThreadMgrEx interface is used by the application to activate the textservices with some flags. ITfThreadMgrEx can be obtained by QI from ITfThreadMgr.
old-location: tsf\itfthreadmgrex.htm
tech.root: TSF
ms.assetid: c230c363-3c62-459f-9350-d96db916f29c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfThreadMgrEx, ITfThreadMgrEx interface [Text Services Framework], ITfThreadMgrEx interface [Text Services Framework],described, _tsf_itfthreadmgrex_ref, msctf/ITfThreadMgrEx, tsf.itfthreadmgrex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.h
api_name:
 - ITfThreadMgrEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfThreadMgrEx interface


## -description


The <b>ITfThreadMgrEx</b> interface is used by the application to activate the textservices with some flags. ITfThreadMgrEx can be obtained by QI from <a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfThreadMgrEx</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfThreadMgrEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfThreadMgrEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3cecc02-5228-4912-a609-f9f3334e11b7">ActivateEx</a>
</td>
<td align="left" width="63%">
Activates TSF for the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b15ddc3-0719-48cf-95fc-9c6d1e15fd4f">GetActiveFlags</a>
</td>
<td align="left" width="63%">
Gets the active flags of the calling thread.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr
      </a>
 

 

