---
UID: NN:msctf.ITfRangeBackup
title: ITfRangeBackup
author: windows-sdk-content
description: The ITfRangeBackup interface is implemented by the TSF manager and is used by a text service to create a backup copy of the data contained in a range object.
old-location: tsf\itfrangebackup.htm
tech.root: TSF
ms.assetid: f98cd8d0-7033-4bd2-94a1-1a75913c2647
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ITfRangeBackup, ITfRangeBackup interface [Text Services Framework], ITfRangeBackup interface [Text Services Framework],described, _tsf_itfrangebackup_ref, msctf/ITfRangeBackup, tsf.itfrangebackup
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
 - ITfRangeBackup
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfRangeBackup interface


## -description


The <b>ITfRangeBackup</b> interface is implemented by the TSF manager and is used by a text service to create a backup copy of the data contained in a range object. This backup copy can be used later to restore the range object. An instance of this interface is obtained by calling <a href="https://msdn.microsoft.com/c3b52170-af1b-407b-9160-1265ae3c9afc">ITfContext::CreateRangeBackup</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfRangeBackup</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfRangeBackup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfRangeBackup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb168504-34c0-4d30-826e-61926fd10a2a">Restore</a>
</td>
<td align="left" width="63%">
Restores a specified range object into the TSF context.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c3b52170-af1b-407b-9160-1265ae3c9afc">ITfContext::CreateRangeBackup
      </a>



<a href="https://msdn.microsoft.com/2b85012f-b090-4c91-b29c-b2470ff63ab6">ITfRange::Clone
      </a>



<a href="_COM_IUnknown">IUnknown</a>



<a href="ranges.htm">Ranges: Clones and Backups</a>
 

 

