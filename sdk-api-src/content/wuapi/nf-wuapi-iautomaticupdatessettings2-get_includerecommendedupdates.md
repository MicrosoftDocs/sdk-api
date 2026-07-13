---
UID: NF:wuapi.IAutomaticUpdatesSettings2.get_IncludeRecommendedUpdates
title: IAutomaticUpdatesSettings2::get_IncludeRecommendedUpdates (wuapi.h)
description: Gets and sets a Boolean value that indicates whether to include optional or recommended updates when a search for updates and installation of updates is performed. (Get)
helpviewer_keywords: ["IAutomaticUpdatesSettings2 interface [Windows Update Agent]","IncludeRecommendedUpdates property","IAutomaticUpdatesSettings2.IncludeRecommendedUpdates","IAutomaticUpdatesSettings2.get_IncludeRecommendedUpdates","IAutomaticUpdatesSettings2::IncludeRecommendedUpdates","IAutomaticUpdatesSettings2::get_IncludeRecommendedUpdates","IAutomaticUpdatesSettings2::put_IncludeRecommendedUpdates","IncludeRecommendedUpdates property [Windows Update Agent]","IncludeRecommendedUpdates property [Windows Update Agent]","IAutomaticUpdatesSettings2 interface","get_IncludeRecommendedUpdates","wua.iautomaticupdatessettings2_includerecommendedupdates","wuapi/IAutomaticUpdatesSettings2::IncludeRecommendedUpdates","wuapi/IAutomaticUpdatesSettings2::get_IncludeRecommendedUpdates","wuapi/IAutomaticUpdatesSettings2::put_IncludeRecommendedUpdates"]
old-location: wua\iautomaticupdatessettings2_includerecommendedupdates.htm
tech.root: wua
ms.assetid: 502b0490-8834-496a-8691-d9325ad86799
ms.date: 12/05/2018
ms.keywords: IAutomaticUpdatesSettings2 interface [Windows Update Agent],IncludeRecommendedUpdates property, IAutomaticUpdatesSettings2.IncludeRecommendedUpdates, IAutomaticUpdatesSettings2.get_IncludeRecommendedUpdates, IAutomaticUpdatesSettings2::IncludeRecommendedUpdates, IAutomaticUpdatesSettings2::get_IncludeRecommendedUpdates, IAutomaticUpdatesSettings2::put_IncludeRecommendedUpdates, IncludeRecommendedUpdates property [Windows Update Agent], IncludeRecommendedUpdates property [Windows Update Agent],IAutomaticUpdatesSettings2 interface, get_IncludeRecommendedUpdates, wua.iautomaticupdatessettings2_includerecommendedupdates, wuapi/IAutomaticUpdatesSettings2::IncludeRecommendedUpdates, wuapi/IAutomaticUpdatesSettings2::get_IncludeRecommendedUpdates, wuapi/IAutomaticUpdatesSettings2::put_IncludeRecommendedUpdates
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
 - IAutomaticUpdatesSettings2::get_IncludeRecommendedUpdates
 - wuapi/IAutomaticUpdatesSettings2::get_IncludeRecommendedUpdates
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
 - IAutomaticUpdatesSettings2.IncludeRecommendedUpdates
 - IAutomaticUpdatesSettings2.get_IncludeRecommendedUpdates
 - IAutomaticUpdatesSettings2.put_IncludeRecommendedUpdates
---

# IAutomaticUpdatesSettings2::get_IncludeRecommendedUpdates


## -description

<p class="CCE_Message">[<b>Set</b> is no longer supported. Also, starting with 
    Windows 10 calls to <b>Get</b> always return <b>VARIANT_TRUE</b> (include recommended updates). ]


Gets and sets a Boolean value that indicates whether to include optional or recommended updates when a  search for updates and installation of updates is performed.



This property is read/write.

## -parameters

## -remarks

Only administrators can set this property.

The caller can modify the settings in  the <a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings2">IAutomaticUpdatesSettings2</a> interface only if the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly">ReadOnly</a> property is <b>VARIANT_TRUE</b>.
The <b>ReadOnly</b> property may change after the <a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-refresh">Refresh</a> method is called.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings2">IAutomaticUpdatesSettings2</a>
