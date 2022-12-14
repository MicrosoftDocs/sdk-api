---
UID: NF:shappmgr.IEnumPublishedApps.Reset
title: IEnumPublishedApps::Reset (shappmgr.h)
description: Resets the enumeration of IPublishedApp objects to the first item.
helpviewer_keywords: ["IEnumPublishedApps interface [Windows Shell]","Reset method","IEnumPublishedApps.Reset","IEnumPublishedApps::Reset","Reset","Reset method [Windows Shell]","Reset method [Windows Shell]","IEnumPublishedApps interface","inet_IEnumPublishedApps_Reset","shappmgr/IEnumPublishedApps::Reset","shell.IEnumPublishedApps_Reset"]
old-location: shell\IEnumPublishedApps_Reset.htm
tech.root: shell
ms.assetid: 007f6636-725a-4af5-ad3f-578f8183a088
ms.date: 12/05/2018
ms.keywords: IEnumPublishedApps interface [Windows Shell],Reset method, IEnumPublishedApps.Reset, IEnumPublishedApps::Reset, Reset, Reset method [Windows Shell], Reset method [Windows Shell],IEnumPublishedApps interface, inet_IEnumPublishedApps_Reset, shappmgr/IEnumPublishedApps::Reset, shell.IEnumPublishedApps_Reset
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
 - IEnumPublishedApps::Reset
 - shappmgr/IEnumPublishedApps::Reset
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
 - IEnumPublishedApps.Reset
---

# IEnumPublishedApps::Reset


## -description

Resets the enumeration of <a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a> objects to the first item.



## -returns

Type: <b>HRESULT</b>

Returns the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
This method only returns S_OK.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  <a href="/windows/desktop/api/shappmgr/nn-shappmgr-ienumpublishedapps">IEnumPublishedApps</a> is not a standard enumeration interface.</div>
<div> </div>
 It does not support a Skip method nor does its Next method support retrieval of multiple items.

## -see-also

<a href="/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ienumpublishedapps">IEnumPublishedApps</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>
