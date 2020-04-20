---
UID: NF:qnetwork.IAMChannelInfo.get_ContactPhone
title: IAMChannelInfo::get_ContactPhone (qnetwork.h)
description: The get_ContactPhone method retrieves the phone number of the contact.helpviewer_keywords: ["IAMChannelInfo interface [DirectShow]","get_ContactPhone method","IAMChannelInfo.get_ContactPhone","IAMChannelInfo::get_ContactPhone","IAMChannelInfoget_ContactPhone","dshow.iamchannelinfo_get_contactphone","get_ContactPhone","get_ContactPhone method [DirectShow]","get_ContactPhone method [DirectShow]","IAMChannelInfo interface","qnetwork/IAMChannelInfo::get_ContactPhone"]
old-location: dshow\iamchannelinfo_get_contactphone.htm
tech.root: DirectShow
ms.assetid: b5addbbb-a0f3-4dec-a347-9c69864a0615
ms.date: 12/05/2018
ms.keywords: IAMChannelInfo interface [DirectShow],get_ContactPhone method, IAMChannelInfo.get_ContactPhone, IAMChannelInfo::get_ContactPhone, IAMChannelInfoget_ContactPhone, dshow.iamchannelinfo_get_contactphone, get_ContactPhone, get_ContactPhone method [DirectShow], get_ContactPhone method [DirectShow],IAMChannelInfo interface, qnetwork/IAMChannelInfo::get_ContactPhone
f1_keywords:
- qnetwork/IAMChannelInfo.get_ContactPhone
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Qnetwork.h
api_name:
- IAMChannelInfo.get_ContactPhone
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMChannelInfo::get_ContactPhone


## -description



The <code>get_ContactPhone</code> method retrieves the phone number of the contact.




## -parameters




### -param pbstrContactPhone [out]

Pointer to a variable that receives the contact's phone number.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nn-qnetwork-iamchannelinfo">IAMChannelInfo Interface</a>
 

 

