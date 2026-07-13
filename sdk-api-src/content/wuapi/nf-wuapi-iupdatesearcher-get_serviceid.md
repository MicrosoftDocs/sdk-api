---
UID: NF:wuapi.IUpdateSearcher.get_ServiceID
title: IUpdateSearcher::get_ServiceID (wuapi.h)
description: Gets and sets a site to search when the site to search is not a Windows Update site. (Get)
helpviewer_keywords: ["IUpdateSearcher interface [Windows Update Agent]","ServiceID property","IUpdateSearcher.ServiceID","IUpdateSearcher.get_ServiceID","IUpdateSearcher::ServiceID","IUpdateSearcher::get_ServiceID","IUpdateSearcher::put_ServiceID","ServiceID property [Windows Update Agent]","ServiceID property [Windows Update Agent]","IUpdateSearcher interface","get_ServiceID","wua.iupdatesearcherserviceid","wuapi/IUpdateSearcher::ServiceID","wuapi/IUpdateSearcher::get_ServiceID","wuapi/IUpdateSearcher::put_ServiceID"]
old-location: wua\iupdatesearcherserviceid.htm
tech.root: wua
ms.assetid: 7c00d26a-9ef0-45ec-81b3-d13f91dd7d8d
ms.date: 12/05/2018
ms.keywords: IUpdateSearcher interface [Windows Update Agent],ServiceID property, IUpdateSearcher.ServiceID, IUpdateSearcher.get_ServiceID, IUpdateSearcher::ServiceID, IUpdateSearcher::get_ServiceID, IUpdateSearcher::put_ServiceID, ServiceID property [Windows Update Agent], ServiceID property [Windows Update Agent],IUpdateSearcher interface, get_ServiceID, wua.iupdatesearcherserviceid, wuapi/IUpdateSearcher::ServiceID, wuapi/IUpdateSearcher::get_ServiceID, wuapi/IUpdateSearcher::put_ServiceID
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
 - IUpdateSearcher::get_ServiceID
 - wuapi/IUpdateSearcher::get_ServiceID
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
 - IUpdateSearcher.ServiceID
 - IUpdateSearcher.get_ServiceID
 - IUpdateSearcher.put_ServiceID
---

# IUpdateSearcher::get_ServiceID


## -description

Gets and sets a site to search when the site to search is not a Windows Update site.

This property is read/write.

## -parameters

## -remarks

The site that is not a Windows Update site that is specified by the value of the <b>ServiceID</b> property is searched only if the value of the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-get_serverselection">ServerSelection</a> property is  ssOthers.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a>
