---
UID: NN:msctf.ITfMouseTracker
title: ITfMouseTracker
author: windows-sdk-content
description: The ITfMouseTracker interface is implemented by the TSF manager and is used by a text service to manage mouse event notification sinks. An instance of this interface is obtained by querying an ITfContext object for IID_ITfMouseTracker.
old-location: tsf\itfmousetracker.htm
old-project: TSF
ms.assetid: aad07b35-99e0-4c76-ba65-93c2c972303d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfMouseTracker, ITfMouseTracker interface [Text Services Framework], ITfMouseTracker interface [Text Services Framework],described, _tsf_itfmousetracker_ref, msctf/ITfMouseTracker, tsf.itfmousetracker
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
 - ITfMouseTracker
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfMouseTracker interface


## -description


The <b>ITfMouseTracker</b> interface is implemented by the TSF manager and is used by a text service to manage mouse event notification sinks. An instance of this interface is obtained by querying an <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> object for IID_ITfMouseTracker.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfMouseTracker</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfMouseTracker</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfMouseTracker</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d73b2b9b-8904-4507-9b32-dcb8946fb887">AdviseMouseSink</a>
</td>
<td align="left" width="63%">
Installs a mouse event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7707b7ce-662b-43e5-ada4-ba42eec56ede">UnadviseMouseSink</a>
</td>
<td align="left" width="63%">
Uninstalls a mouse event sink.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

