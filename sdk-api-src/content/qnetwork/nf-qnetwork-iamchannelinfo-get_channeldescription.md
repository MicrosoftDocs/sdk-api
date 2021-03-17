---
UID: NF:qnetwork.IAMChannelInfo.get_ChannelDescription
title: IAMChannelInfo::get_ChannelDescription (qnetwork.h)
description: The get_ChannelDescription method retrieves the description of the channel.
helpviewer_keywords: ["IAMChannelInfo interface [DirectShow]","get_ChannelDescription method","IAMChannelInfo.get_ChannelDescription","IAMChannelInfo::get_ChannelDescription","IAMChannelInfoget_ChannelDescription","dshow.iamchannelinfo_get_channeldescription","get_ChannelDescription","get_ChannelDescription method [DirectShow]","get_ChannelDescription method [DirectShow]","IAMChannelInfo interface","qnetwork/IAMChannelInfo::get_ChannelDescription"]
old-location: dshow\iamchannelinfo_get_channeldescription.htm
tech.root: dshow
ms.assetid: c39b15af-0766-4512-9720-4cdaef6120ba
ms.date: 12/05/2018
ms.keywords: IAMChannelInfo interface [DirectShow],get_ChannelDescription method, IAMChannelInfo.get_ChannelDescription, IAMChannelInfo::get_ChannelDescription, IAMChannelInfoget_ChannelDescription, dshow.iamchannelinfo_get_channeldescription, get_ChannelDescription, get_ChannelDescription method [DirectShow], get_ChannelDescription method [DirectShow],IAMChannelInfo interface, qnetwork/IAMChannelInfo::get_ChannelDescription
req.header: qnetwork.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMChannelInfo::get_ChannelDescription
 - qnetwork/IAMChannelInfo::get_ChannelDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMChannelInfo.get_ChannelDescription
---

# IAMChannelInfo::get_ChannelDescription


## -description

The <code>get_ChannelDescription</code> method retrieves the description of the channel.

## -parameters

### -param pbstrChannelDescription [out]

Receives the channel description.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamchannelinfo">IAMChannelInfo Interface</a>