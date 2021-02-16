---
UID: NF:contentpartner.IWMPContentContainerList.GetTransactionType
title: IWMPContentContainerList::GetTransactionType (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The GetTransactionType method retrieves the type of the current transaction.
helpviewer_keywords: ["GetTransactionType","GetTransactionType method [Windows Media Player]","GetTransactionType method [Windows Media Player]","IWMPContentContainerList interface","IWMPContentContainerList interface [Windows Media Player]","GetTransactionType method","IWMPContentContainerList.GetTransactionType","IWMPContentContainerList::GetTransactionType","IWMPContentContainerListGetTransactionType","contentpartner/IWMPContentContainerList::GetTransactionType","wmp.iwmpcontentcontainerlist_gettransactiontype"]
old-location: wmp\iwmpcontentcontainerlist_gettransactiontype.htm
tech.root: WMP
ms.assetid: 8712d134-9dd3-4964-ae53-f63c8b69818d
ms.date: 12/05/2018
ms.keywords: GetTransactionType, GetTransactionType method [Windows Media Player], GetTransactionType method [Windows Media Player],IWMPContentContainerList interface, IWMPContentContainerList interface [Windows Media Player],GetTransactionType method, IWMPContentContainerList.GetTransactionType, IWMPContentContainerList::GetTransactionType, IWMPContentContainerListGetTransactionType, contentpartner/IWMPContentContainerList::GetTransactionType, wmp.iwmpcontentcontainerlist_gettransactiontype
req.header: contentpartner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
req.target-min-winversvr: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPContentContainerList::GetTransactionType
 - contentpartner/IWMPContentContainerList::GetTransactionType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - contentpartner.h
api_name:
 - IWMPContentContainerList.GetTransactionType
---

# IWMPContentContainerList::GetTransactionType


## -description

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetTransactionType</b> method retrieves the type of the current transaction.

## -parameters

### -param pwmptt [out]

Pointer to a <a href="/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype">WMPTransactionType</a> that receives the transaction type value.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist">IWMPContentContainerList Interface</a>



<a href="/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype">WMPTransactionType</a>