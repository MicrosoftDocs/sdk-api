---
UID: NF:contentpartner.IWMPContentContainerList.GetTransactionType
title: IWMPContentContainerList::GetTransactionType (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The GetTransactionType method retrieves the type of the current transaction.
helpviewer_keywords: ["GetTransactionType","GetTransactionType method [Windows Media Player]","GetTransactionType method [Windows Media Player]","IWMPContentContainerList interface","IWMPContentContainerList interface [Windows Media Player]","GetTransactionType method","IWMPContentContainerList.GetTransactionType","IWMPContentContainerList::GetTransactionType","IWMPContentContainerListGetTransactionType","contentpartner/IWMPContentContainerList::GetTransactionType","wmp.iwmpcontentcontainerlist_gettransactiontype"]
old-location: wmp\iwmpcontentcontainerlist_gettransactiontype.htm
tech.root: WMP
ms.assetid: 8712d134-9dd3-4964-ae53-f63c8b69818d
ms.date: 4/26/2023
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

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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