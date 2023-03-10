---
UID: NF:qnetwork.IDShowPlugin.get_URL
title: IDShowPlugin::get_URL (qnetwork.h)
description: The get_URL method retrieves the URL of the current web page.
helpviewer_keywords: ["IDShowPlugin interface [DirectShow]","get_URL method","IDShowPlugin.get_URL","IDShowPlugin::get_URL","IDShowPluginget_URL","dshow.idshowplugin_get_url","get_URL","get_URL method [DirectShow]","get_URL method [DirectShow]","IDShowPlugin interface","qnetwork/IDShowPlugin::get_URL"]
old-location: dshow\idshowplugin_get_url.htm
tech.root: dshow
ms.assetid: df1a2643-c89e-4edf-bd85-bce1c410d6cd
ms.date: 12/05/2018
ms.keywords: IDShowPlugin interface [DirectShow],get_URL method, IDShowPlugin.get_URL, IDShowPlugin::get_URL, IDShowPluginget_URL, dshow.idshowplugin_get_url, get_URL, get_URL method [DirectShow], get_URL method [DirectShow],IDShowPlugin interface, qnetwork/IDShowPlugin::get_URL
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDShowPlugin::get_URL
 - qnetwork/IDShowPlugin::get_URL
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
 - IDShowPlugin.get_URL
---

# IDShowPlugin::get_URL


## -description

The <b>get_URL</b> method retrieves the URL of the current web page.

## -parameters

### -param pURL

Receives the URL.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The caller must release the returned <b>BSTR</b>, by calling <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-idshowplugin">IDShowPlugin Interface</a>