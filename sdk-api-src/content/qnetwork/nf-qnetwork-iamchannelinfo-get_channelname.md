---
UID: NF:qnetwork.IAMChannelInfo.get_ChannelName
title: IAMChannelInfo::get_ChannelName (qnetwork.h)
description: The get_ChannelName method retrieves the channel name.
helpviewer_keywords: ["IAMChannelInfo interface [DirectShow]","get_ChannelName method","IAMChannelInfo.get_ChannelName","IAMChannelInfo::get_ChannelName","IAMChannelInfoget_ChannelName","dshow.iamchannelinfo_get_channelname","get_ChannelName","get_ChannelName method [DirectShow]","get_ChannelName method [DirectShow]","IAMChannelInfo interface","qnetwork/IAMChannelInfo::get_ChannelName"]
old-location: dshow\iamchannelinfo_get_channelname.htm
tech.root: dshow
ms.assetid: 6cf4f8aa-d6aa-46bd-83b1-fba762fbb8bb
ms.date: 12/05/2018
ms.keywords: IAMChannelInfo interface [DirectShow],get_ChannelName method, IAMChannelInfo.get_ChannelName, IAMChannelInfo::get_ChannelName, IAMChannelInfoget_ChannelName, dshow.iamchannelinfo_get_channelname, get_ChannelName, get_ChannelName method [DirectShow], get_ChannelName method [DirectShow],IAMChannelInfo interface, qnetwork/IAMChannelInfo::get_ChannelName
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
 - IAMChannelInfo::get_ChannelName
 - qnetwork/IAMChannelInfo::get_ChannelName
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
 - IAMChannelInfo.get_ChannelName
---

# IAMChannelInfo::get_ChannelName


## -description

The <code>get_ChannelName</code> method retrieves the channel name.

## -parameters

### -param pbstrChannelName [out]

Pointer to a variable that receives a string containing the channel name.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamchannelinfo">IAMChannelInfo Interface</a>