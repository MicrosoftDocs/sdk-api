---
UID: NF:qnetwork.IDShowPlugin.get_UserAgent
title: IDShowPlugin::get_UserAgent (qnetwork.h)
description: The get_UserAgent method retrieves the User-Agent field from the HTTP header.helpviewer_keywords: ["IDShowPlugin interface [DirectShow]","get_UserAgent method","IDShowPlugin.get_UserAgent","IDShowPlugin::get_UserAgent","IDShowPluginget_UserAgent","dshow.idshowplugin_get_useragent","get_UserAgent","get_UserAgent method [DirectShow]","get_UserAgent method [DirectShow]","IDShowPlugin interface","qnetwork/IDShowPlugin::get_UserAgent"]
old-location: dshow\idshowplugin_get_useragent.htm
tech.root: DirectShow
ms.assetid: 0bbd3cd2-75d8-4c48-837d-4cb045cad35b
ms.date: 12/05/2018
ms.keywords: IDShowPlugin interface [DirectShow],get_UserAgent method, IDShowPlugin.get_UserAgent, IDShowPlugin::get_UserAgent, IDShowPluginget_UserAgent, dshow.idshowplugin_get_useragent, get_UserAgent, get_UserAgent method [DirectShow], get_UserAgent method [DirectShow],IDShowPlugin interface, qnetwork/IDShowPlugin::get_UserAgent
f1_keywords:
- qnetwork/IDShowPlugin.get_UserAgent
dev_langs:
- c++
req.header: qnetwork.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- IDShowPlugin.get_UserAgent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDShowPlugin::get_UserAgent


## -description



The <code>get_UserAgent</code> method retrieves the User-Agent field from the HTTP header.




## -parameters




### -param pUserAgent

Pointer to a variable that receives the User-Agent string.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The caller must release the returned <b>BSTR</b>, by calling <b>SysFreeString</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nn-qnetwork-idshowplugin">IDShowPlugin Interface</a>
 

 

