---
UID: NN:msctf.ITfEditSession
title: ITfEditSession
author: windows-sdk-content
description: The ITfEditSession interface is implemented by a text service and used by the TSF manager to read and/or modify the text and properties of a context.
old-location: tsf\itfeditsession.htm
old-project: TSF
ms.assetid: b9d4718a-42a6-4be5-9f57-1a392cd98469
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfEditSession, ITfEditSession interface [Text Services Framework], ITfEditSession interface [Text Services Framework],described, _tsf_itfeditsession_ref, msctf/ITfEditSession, tsf.itfeditsession
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
 - tipskins.dll
api_name:
 - ITfEditSession
product: Windows
targetos: Windows
req.lib: 
req.dll: Tipskins.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfEditSession interface


## -description


The <b>ITfEditSession</b> interface is implemented by a text service and used by the TSF manager to read and/or modify the text and properties of a context.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfEditSession</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfEditSession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfEditSession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">DoEditSession</a>
</td>
<td align="left" width="63%">
Called to enable a text service to read and/or modify the contents of a context.

</td>
</tr>
</table> 


## -remarks



A text service initiates an edit session by calling <a href="https://msdn.microsoft.com/6c7b150c-0ca0-4aa5-8828-0c548dbfb215">ITfContext::RequestEditSession</a>, passing a pointer to the <b>ITfEditSession</b> interface. When the edit session is granted, the TSF manager calls <b>DoEditSession</b>.

If the context is destroyed before the application grants a lock, or if the calling text service is deactivated before a lock is granted, the <b>DoEditSession</b> method is not called. For this reason, a text service should put cleanup operations for an edit session in the <b>ITfEditSession</b> interface destructor rather than in the <b>DoEditSession</b> method.




## -see-also




<a href="https://msdn.microsoft.com/e4115227-1036-4892-986d-dc4cef5b178e">Edit Sessions</a>



<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/6c7b150c-0ca0-4aa5-8828-0c548dbfb215">ITfContext::RequestEditSession
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

