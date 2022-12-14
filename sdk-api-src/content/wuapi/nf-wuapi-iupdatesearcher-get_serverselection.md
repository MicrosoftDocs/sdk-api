---
UID: NF:wuapi.IUpdateSearcher.get_ServerSelection
title: IUpdateSearcher::get_ServerSelection (wuapi.h)
description: Gets and sets a ServerSelection value that indicates the server to search for updates. (Get)
helpviewer_keywords: ["IUpdateSearcher interface [Windows Update Agent]","ServerSelection property","IUpdateSearcher.ServerSelection","IUpdateSearcher.get_ServerSelection","IUpdateSearcher::ServerSelection","IUpdateSearcher::get_ServerSelection","IUpdateSearcher::put_ServerSelection","ServerSelection property [Windows Update Agent]","ServerSelection property [Windows Update Agent]","IUpdateSearcher interface","get_ServerSelection","wua.iupdatesearcherserverselection","wuapi/IUpdateSearcher::ServerSelection","wuapi/IUpdateSearcher::get_ServerSelection","wuapi/IUpdateSearcher::put_ServerSelection"]
old-location: wua\iupdatesearcherserverselection.htm
tech.root: wua
ms.assetid: b514545a-d983-491b-9a28-540bd5c4c128
ms.date: 12/05/2018
ms.keywords: IUpdateSearcher interface [Windows Update Agent],ServerSelection property, IUpdateSearcher.ServerSelection, IUpdateSearcher.get_ServerSelection, IUpdateSearcher::ServerSelection, IUpdateSearcher::get_ServerSelection, IUpdateSearcher::put_ServerSelection, ServerSelection property [Windows Update Agent], ServerSelection property [Windows Update Agent],IUpdateSearcher interface, get_ServerSelection, wua.iupdatesearcherserverselection, wuapi/IUpdateSearcher::ServerSelection, wuapi/IUpdateSearcher::get_ServerSelection, wuapi/IUpdateSearcher::put_ServerSelection
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
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
 - IUpdateSearcher::get_ServerSelection
 - wuapi/IUpdateSearcher::get_ServerSelection
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
 - IUpdateSearcher.ServerSelection
 - IUpdateSearcher.get_ServerSelection
 - IUpdateSearcher.put_ServerSelection
---

# IUpdateSearcher::get_ServerSelection


## -description

Gets and sets a <a href="/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a">ServerSelection</a> value that indicates the server to search for updates.

This property is read/write.

## -parameters

## -remarks

 The site that is not a Windows Update site that is specified by the value of the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-get_serviceid">ServiceID</a> property is searched only if the value of the <b>ServerSelection</b> property is  ssOthers.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a>
