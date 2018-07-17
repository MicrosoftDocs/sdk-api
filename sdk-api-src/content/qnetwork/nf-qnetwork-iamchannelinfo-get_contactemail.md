---
UID: NF:qnetwork.IAMChannelInfo.get_ContactEmail
title: IAMChannelInfo::get_ContactEmail
author: windows-sdk-content
description: The get_ContactEmail method gets the email address of the contact.
old-location: dshow\iamchannelinfo_get_contactemail.htm
old-project: DirectShow
ms.assetid: a8ab9fc0-1370-44a1-95c8-6592c374d8d6
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IAMChannelInfo interface [DirectShow],get_ContactEmail method, IAMChannelInfo.get_ContactEmail, IAMChannelInfo::get_ContactEmail, IAMChannelInfoget_ContactEmail, dshow.iamchannelinfo_get_contactemail, get_ContactEmail, get_ContactEmail method [DirectShow], get_ContactEmail method [DirectShow],IAMChannelInfo interface, qnetwork/IAMChannelInfo::get_ContactEmail
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
tech.root: 
req.typenames: AMExtendedSeekingCapabilities
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMChannelInfo.get_ContactEmail
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IAMChannelInfo::get_ContactEmail


## -description



The <b>get_ContactEmail</b> method gets the email address of the contact.




## -parameters




### -param pbstrContactEmail [out]

Receives the contact email.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.




## -see-also




<a href="https://msdn.microsoft.com/779d1c0a-f838-4d02-8254-d66916d3b790">IAMChannelInfo Interface</a>
 

 

