---
UID: NN:shappmgr.IPublishedApp
title: IPublishedApp (shappmgr.h)
description: Exposes methods that represent applications to Add/Remove Programs in Control Panel.
helpviewer_keywords: ["IPublishedApp","IPublishedApp interface [Windows Shell]","IPublishedApp interface [Windows Shell]","described","inet_IPublishedApp","shappmgr/IPublishedApp","shell.IPublishedApp"]
old-location: shell\IPublishedApp.htm
tech.root: shell
ms.assetid: a5a44e74-494a-4c9b-8bf3-85c6093b2c0e
ms.date: 12/05/2018
ms.keywords: IPublishedApp, IPublishedApp interface [Windows Shell], IPublishedApp interface [Windows Shell],described, inet_IPublishedApp, shappmgr/IPublishedApp, shell.IPublishedApp
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
 - IPublishedApp
 - shappmgr/IPublishedApp
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
 - IPublishedApp
---

# IPublishedApp interface


## -description

Exposes methods that represent applications to Add/Remove Programs in Control Panel.

## -inheritance

The <b>IPublishedApp</b> interface inherits from <a href="/windows/desktop/api/shappmgr/nn-shappmgr-ishellapp">IShellApp</a>. <b>IPublishedApp</b> also has these types of members:

## -remarks

To publish applications to Add/Remove Programs in Control Panel, you must support <a href="/windows/desktop/api/shappmgr/nn-shappmgr-ienumpublishedapps">IEnumPublishedApps</a>, <a href="/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a> and <b>IPublishedApp</b>.

## -see-also

<a href="/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ienumpublishedapps">IEnumPublishedApps</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ishellapp">IShellApp</a>
