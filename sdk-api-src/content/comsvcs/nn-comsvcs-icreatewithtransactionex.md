---
UID: NN:comsvcs.ICreateWithTransactionEx
title: ICreateWithTransactionEx
author: windows-driver-content
description: Creates an object that is enlisted within a manual transaction.
old-location: cos\icreatewithtransactionex.htm
old-project: cossdk
ms.assetid: 39b455d3-d3d2-46ae-a45e-b036c18e45bc
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ICreateWithTransactionEx, ICreateWithTransactionEx interface [COM+], ICreateWithTransactionEx interface [COM+], described, _dtc_ICreateWithTransactionEx_Interface, comsvcs/ICreateWithTransactionEx, cos.icreatewithtransactionex
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	ICreateWithTransactionEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICreateWithTransactionEx interface


## -description


Creates an object that is enlisted within a manual transaction.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreateWithTransactionEx</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICreateWithTransactionEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICreateWithTransactionEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71d3b8ad-195b-47a6-8197-05df6311ed2a">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates a COM+ object that executes within the scope of a manual transaction specified with a reference to an <b>ITransaction</b> interface.

</td>
</tr>
</table> 

