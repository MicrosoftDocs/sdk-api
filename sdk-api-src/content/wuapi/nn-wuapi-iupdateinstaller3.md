---
UID: NN:wuapi.IUpdateInstaller3
title: IUpdateInstaller3 (wuapi.h)
description: Installs or uninstalls updates on a computer. (IUpdateInstaller3)
helpviewer_keywords: ["IUpdateInstaller3","IUpdateInstaller3 interface [Windows Update Agent]","IUpdateInstaller3 interface [Windows Update Agent]","described","wua.iupdateinstaller3","wuapi/IUpdateInstaller3"]
old-location: wua\iupdateinstaller3.htm
tech.root: wua
ms.assetid: 5A237B5C-A07B-470F-B2F6-ABC936DCE1A5
ms.date: 12/05/2018
ms.keywords: IUpdateInstaller3, IUpdateInstaller3 interface [Windows Update Agent], IUpdateInstaller3 interface [Windows Update Agent],described, wua.iupdateinstaller3, wuapi/IUpdateInstaller3
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdateInstaller3
 - wuapi/IUpdateInstaller3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateInstaller3
---

# IUpdateInstaller3 interface


## -description

<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]
<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Installs or uninstalls updates on a computer. This property is only used when installing Microsoft Store app updates. It has no effect when installing non-Microsoft Store app updates such as operating system, Defender, or driver updates.

## -inheritance

The <b>IUpdateInstaller3</b> interface inherits from <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateinstaller2">IUpdateInstaller2</a>. <b>IUpdateInstaller3</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateinstaller2">IUpdateInstaller2</a>
