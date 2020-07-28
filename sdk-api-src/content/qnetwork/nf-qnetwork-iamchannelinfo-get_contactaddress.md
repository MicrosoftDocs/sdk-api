---
UID: NF:qnetwork.IAMChannelInfo.get_ContactAddress
title: IAMChannelInfo::get_ContactAddress (qnetwork.h)
description: The get_ContactAddress method retrieves the contact address.
helpviewer_keywords: ["IAMChannelInfo interface [DirectShow]","get_ContactAddress method","IAMChannelInfo.get_ContactAddress","IAMChannelInfo::get_ContactAddress","IAMChannelInfoget_ContactAddress","dshow.iamchannelinfo_get_contactaddress","get_ContactAddress","get_ContactAddress method [DirectShow]","get_ContactAddress method [DirectShow]","IAMChannelInfo interface","qnetwork/IAMChannelInfo::get_ContactAddress"]
old-location: dshow\iamchannelinfo_get_contactaddress.htm
tech.root: dshow
ms.assetid: b94ccc71-92d1-4c1a-b34a-c34e6ea7bd91
ms.date: 12/05/2018
ms.keywords: IAMChannelInfo interface [DirectShow],get_ContactAddress method, IAMChannelInfo.get_ContactAddress, IAMChannelInfo::get_ContactAddress, IAMChannelInfoget_ContactAddress, dshow.iamchannelinfo_get_contactaddress, get_ContactAddress, get_ContactAddress method [DirectShow], get_ContactAddress method [DirectShow],IAMChannelInfo interface, qnetwork/IAMChannelInfo::get_ContactAddress
f1_keywords:
- qnetwork/IAMChannelInfo.get_ContactAddress
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
- IAMChannelInfo.get_ContactAddress
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMChannelInfo::get_ContactAddress


## -description



The <code>get_ContactAddress</code> method retrieves the contact address.




## -parameters




### -param pbstrContactAddress [out]

Pointer to a variable that receives the contact address.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nn-qnetwork-iamchannelinfo">IAMChannelInfo Interface</a>
 

 

