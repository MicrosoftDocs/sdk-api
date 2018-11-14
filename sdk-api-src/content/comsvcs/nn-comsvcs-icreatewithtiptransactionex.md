---
UID: NN:comsvcs.ICreateWithTipTransactionEx
title: ICreateWithTipTransactionEx
author: windows-sdk-content
description: Creates an object that is enlisted within a manual transaction using the Transaction Internet Protocol (TIP).
old-location: cos\icreatewithtiptransactionex.htm
tech.root: cossdk
ms.assetid: 09927c61-ce64-4d8a-a5b3-542748bfd256
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICreateWithTipTransactionEx, ICreateWithTipTransactionEx interface [COM+], ICreateWithTipTransactionEx interface [COM+],described, _dtc_ICreateWithTipTransactionEx_Interface, comsvcs/ICreateWithTipTransactionEx, cos.icreatewithtiptransactionex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - ComSvcs.h
api_name:
 - ICreateWithTipTransactionEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICreateWithTipTransactionEx interface


## -description


<p class="CCE_Message">[The TIP service feature are deprecated and might not be available in future versions of the operating system. Consider using the WS-AtomicTransaction (WS-AT) protocol as a replacement transaction coordination and propagation technology. For more information about WS-AT support in the .Net Framework, see <a href="http://go.microsoft.com/fwlink/p/?linkid=105715">Transactions</a>.]

Creates an object that is enlisted within a manual transaction using the Transaction Internet Protocol (TIP).



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreateWithTipTransactionEx</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICreateWithTipTransactionEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICreateWithTipTransactionEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f0572eb-8633-4dc3-a013-9cf859241cd7">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates a COM+ object that executes within the scope of the manual transaction specified by a TIP transaction URL.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/39b455d3-d3d2-46ae-a45e-b036c18e45bc">ICreateWithTransactionEx</a>
 

 

