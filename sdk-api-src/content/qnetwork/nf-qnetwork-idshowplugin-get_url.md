---
UID: NF:qnetwork.IDShowPlugin.get_URL
title: IDShowPlugin::get_URL
author: windows-sdk-content
description: The get_URL method retrieves the URL of the current web page.
old-location: dshow\idshowplugin_get_url.htm
tech.root: DirectShow
ms.assetid: df1a2643-c89e-4edf-bd85-bce1c410d6cd
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IDShowPlugin interface [DirectShow],get_URL method, IDShowPlugin.get_URL, IDShowPlugin::get_URL, IDShowPluginget_URL, dshow.idshowplugin_get_url, get_URL, get_URL method [DirectShow], get_URL method [DirectShow],IDShowPlugin interface, qnetwork/IDShowPlugin::get_URL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDShowPlugin.get_URL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDShowPlugin::get_URL


## -description



The <b>get_URL</b> method retrieves the URL of the current web page.




## -parameters




### -param pURL

Receives the URL.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The caller must release the returned <b>BSTR</b>, by calling <b>SysFreeString</b>.




## -see-also




<a href="https://msdn.microsoft.com/b5b73489-4d2d-4afa-a4df-7b84711f2556">IDShowPlugin Interface</a>
 

 

