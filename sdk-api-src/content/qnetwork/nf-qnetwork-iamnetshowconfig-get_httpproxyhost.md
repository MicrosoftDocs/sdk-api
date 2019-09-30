---
UID: NF:qnetwork.IAMNetShowConfig.get_HTTPProxyHost
title: IAMNetShowConfig::get_HTTPProxyHost (qnetwork.h)
author: windows-sdk-content
description: The get_HTTPProxyHost method retrieves the HTTP address of the proxy host.
old-location: dshow\iamnetshowconfig_get_httpproxyhost.htm
tech.root: DirectShow
ms.assetid: d73aefda-2c51-466a-b590-c8f189db4719
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMNetShowConfig interface [DirectShow],get_HTTPProxyHost method, IAMNetShowConfig.get_HTTPProxyHost, IAMNetShowConfig::get_HTTPProxyHost, IAMNetShowConfigget_HTTPProxyHost, dshow.iamnetshowconfig_get_httpproxyhost, get_HTTPProxyHost, get_HTTPProxyHost method [DirectShow], get_HTTPProxyHost method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::get_HTTPProxyHost
ms.topic: method
f1_keywords: 
 - "qnetwork/IAMNetShowConfig.get_HTTPProxyHost"
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
 - IAMNetShowConfig.get_HTTPProxyHost
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMNetShowConfig::get_HTTPProxyHost


## -description



The <code>get_HTTPProxyHost</code> method retrieves the HTTP address of the proxy host.




## -parameters




### -param pbstrHTTPProxyHost

Pointer to a variable that receives the HTTP address.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The caller must release the returned <b>BSTR</b>, by calling <b>SysFreeString</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowconfig-get_httpproxyport">IAMNetShowConfig::get_HTTPProxyPort</a>
 

 

