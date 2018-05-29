---
UID: NF:qnetwork.IAMChannelInfo.get_ContactPhone
title: IAMChannelInfo::get_ContactPhone
author: windows-sdk-content
description: The get_ContactPhone method retrieves the phone number of the contact.
old-location: dshow\iamchannelinfo_get_contactphone.htm
old-project: DirectShow
ms.assetid: b5addbbb-a0f3-4dec-a347-9c69864a0615
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IAMChannelInfo interface [DirectShow],get_ContactPhone method, IAMChannelInfo.get_ContactPhone, IAMChannelInfo::get_ContactPhone, IAMChannelInfoget_ContactPhone, dshow.iamchannelinfo_get_contactphone, get_ContactPhone, get_ContactPhone method [DirectShow], get_ContactPhone method [DirectShow],IAMChannelInfo interface, qnetwork/IAMChannelInfo::get_ContactPhone
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: AMExtendedSeekingCapabilities
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Qnetwork.h
api_name:
-	IAMChannelInfo.get_ContactPhone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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




<a href="https://msdn.microsoft.com/779d1c0a-f838-4d02-8254-d66916d3b790">IAMChannelInfo Interface</a>
 

 

