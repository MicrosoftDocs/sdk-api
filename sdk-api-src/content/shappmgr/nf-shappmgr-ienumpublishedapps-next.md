---
UID: NF:shappmgr.IEnumPublishedApps.Next
title: IEnumPublishedApps::Next (shappmgr.h)
description: Gets the next IPublishedApp object in the enumeration.
helpviewer_keywords: ["IEnumPublishedApps interface [Windows Shell]","Next method","IEnumPublishedApps.Next","IEnumPublishedApps::Next","Next","Next method [Windows Shell]","Next method [Windows Shell]","IEnumPublishedApps interface","inet_IEnumPublishedApps_Next","shappmgr/IEnumPublishedApps::Next","shell.IEnumPublishedApps_Next"]
old-location: shell\IEnumPublishedApps_Next.htm
tech.root: shell
ms.assetid: 78d18529-2eeb-4510-8703-457ffe998bc5
ms.date: 12/05/2018
ms.keywords: IEnumPublishedApps interface [Windows Shell],Next method, IEnumPublishedApps.Next, IEnumPublishedApps::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumPublishedApps interface, inet_IEnumPublishedApps_Next, shappmgr/IEnumPublishedApps::Next, shell.IEnumPublishedApps_Next
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
 - IEnumPublishedApps::Next
 - shappmgr/IEnumPublishedApps::Next
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
 - IEnumPublishedApps.Next
---

# IEnumPublishedApps::Next


## -description

Gets the next <a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a> object in the enumeration.

## -parameters

### -param pia [out]

Type: <b><a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>**</b>

A pointer to an <a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a> interface reference variable that returns the next application object. Note that the category of the application object returned must match that passed into <a href="/windows/desktop/api/shappmgr/nf-shappmgr-iapppublisher-enumapps">EnumApps</a>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if an item is returned, S_FALSE if there are no more items to enumerate, a COM-defined error value otherwise.

## -remarks

<div class="alert"><b>Note</b>  <a href="/windows/desktop/api/shappmgr/nn-shappmgr-ienumpublishedapps">IEnumPublishedApps</a> is not a standard enumeration interface. It does not support a Skip method, nor does its Next method support retrieval of multiple items.
        </div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ienumpublishedapps">IEnumPublishedApps</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>