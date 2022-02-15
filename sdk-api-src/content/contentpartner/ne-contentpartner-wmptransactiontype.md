---
UID: NE:contentpartner.WMPTransactionType
title: WMPTransactionType (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The WMPTransactionType enumeration represents a transaction type.
helpviewer_keywords: ["WMPTransactionType","WMPTransactionType enumeration [Windows Media Player]","contentpartner/WMPTransactionType","contentpartner/wmpttBuy","contentpartner/wmpttDownload","contentpartner/wmpttNoTransaction","enumeration [Windows Media Player]","wmp.wmptransactiontype","wmpttBuy","wmpttDownload","wmpttNoTransaction"]
old-location: wmp\wmptransactiontype.htm
tech.root: WMP
ms.assetid: b3dc35d8-098a-464d-957e-3746447156d0
ms.date: 12/05/2018
ms.keywords: WMPTransactionType, WMPTransactionType enumeration [Windows Media Player], contentpartner/WMPTransactionType, contentpartner/wmpttBuy, contentpartner/wmpttDownload, contentpartner/wmpttNoTransaction, enumeration [Windows Media Player], wmp.wmptransactiontype, wmpttBuy, wmpttDownload, wmpttNoTransaction
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
req.typenames: WMPTransactionType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPTransactionType
 - contentpartner/WMPTransactionType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - contentpartner.h
api_name:
 - WMPTransactionType
---

# WMPTransactionType enumeration


## -description

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>WMPTransactionType</b> enumeration represents a transaction type.

## -enum-fields

### -field wmpttNoTransaction:0

No transaction.

### -field wmpttDownload:1

A download transaction.

### -field wmpttBuy:2

A purchase transaction.

## -see-also

<a href="/windows/desktop/WMP/enumerations-for-type-1-online-stores">Enumerations for Type 1 Online Stores</a>



<a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype">IWMPContentContainerList::GetTransactionType</a>
