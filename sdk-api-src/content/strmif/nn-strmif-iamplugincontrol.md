---
UID: NN:strmif.IAMPluginControl
title: IAMPluginControl (strmif.h)
description: Controls the preferred and blocked filter lists.
helpviewer_keywords: ["IAMPluginControl","IAMPluginControl interface [DirectShow]","IAMPluginControl interface [DirectShow]","described","dshow.iamplugincontrol","strmif/IAMPluginControl"]
old-location: dshow\iamplugincontrol.htm
tech.root: dshow
ms.assetid: 66720991-3a3f-4c45-a543-b8050d31fcc3
ms.date: 12/05/2018
ms.keywords: IAMPluginControl, IAMPluginControl interface [DirectShow], IAMPluginControl interface [DirectShow],described, dshow.iamplugincontrol, strmif/IAMPluginControl
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IAMPluginControl
 - strmif/IAMPluginControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMPluginControl
---

# IAMPluginControl interface


## -description

Controls the preferred and blocked filter lists.

To get a pointer to this interface, call <b>CoCreateInstance</b>. The class identifier (CLSID) is <b>CLSID_DirectShowPluginControl</b>, which is defined in the header file uuids.h.

## -inheritance

The <b>IAMPluginControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMPluginControl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/intelligent-connect">Intelligent Connect</a>
