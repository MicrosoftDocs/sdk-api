---
UID: NN:shappmgr.IEnumPublishedApps
title: IEnumPublishedApps (shappmgr.h)
description: Exposes methods that enumerate published applications to Add/Remove Programs in the Control Panel. The object exposing this interface is requested through IAppPublisher::EnumApps.
helpviewer_keywords: ["IEnumPublishedApps","IEnumPublishedApps interface [Windows Shell]","IEnumPublishedApps interface [Windows Shell]","described","inet_IEnumPublishedApps","shappmgr/IEnumPublishedApps","shell.IEnumPublishedApps"]
old-location: shell\IEnumPublishedApps.htm
tech.root: shell
ms.assetid: 89a06b1d-1b72-46ca-91cd-bb63ea0cbff7
ms.date: 12/05/2018
ms.keywords: IEnumPublishedApps, IEnumPublishedApps interface [Windows Shell], IEnumPublishedApps interface [Windows Shell],described, inet_IEnumPublishedApps, shappmgr/IEnumPublishedApps, shell.IEnumPublishedApps
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
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
 - IEnumPublishedApps
 - shappmgr/IEnumPublishedApps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shappmgr.h
api_name:
 - IEnumPublishedApps
---

# IEnumPublishedApps interface


## -description

Exposes methods that enumerate published applications to Add/Remove Programs in the Control Panel. The object exposing this interface is requested through <a href="/windows/desktop/api/shappmgr/nf-shappmgr-iapppublisher-enumapps">IAppPublisher::EnumApps</a>.

## -inheritance

The <b>IEnumPublishedApps</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumPublishedApps</b> also has these types of members:

## -remarks

To publish applications to Add/Remove Programs in the Control Panel, you must support <b>IEnumPublishedApps</b>, <a href="/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a> and <a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>.

## -see-also

<a href="/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>
