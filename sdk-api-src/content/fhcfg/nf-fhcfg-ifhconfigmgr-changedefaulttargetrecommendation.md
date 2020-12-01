---
UID: NF:fhcfg.IFhConfigMgr.ChangeDefaultTargetRecommendation
title: IFhConfigMgr::ChangeDefaultTargetRecommendation (fhcfg.h)
description: Causes the currently assigned backup target to be recommended or not recommended to other members of the home group that the computer belongs to.
helpviewer_keywords: ["ChangeDefaultTargetRecommendation","ChangeDefaultTargetRecommendation method [Windows API]","ChangeDefaultTargetRecommendation method [Windows API]","FhConfigMgr class","ChangeDefaultTargetRecommendation method [Windows API]","IFhConfigMgr interface","FhConfigMgr class [Windows API]","ChangeDefaultTargetRecommendation method","IFhConfigMgr interface [Windows API]","ChangeDefaultTargetRecommendation method","IFhConfigMgr.ChangeDefaultTargetRecommendation","IFhConfigMgr::ChangeDefaultTargetRecommendation","fhcfg/IFhConfigMgr::ChangeDefaultTargetRecommendation","winprog.ifhconfigmgr_changedefaulttargetrecommendation"]
old-location: winprog\ifhconfigmgr_changedefaulttargetrecommendation.htm
tech.root: winprog
ms.assetid: 40F22464-FE28-40A0-85C6-74C5BD819E83
ms.date: 12/05/2018
ms.keywords: ChangeDefaultTargetRecommendation, ChangeDefaultTargetRecommendation method [Windows API], ChangeDefaultTargetRecommendation method [Windows API],FhConfigMgr class, ChangeDefaultTargetRecommendation method [Windows API],IFhConfigMgr interface, FhConfigMgr class [Windows API],ChangeDefaultTargetRecommendation method, IFhConfigMgr interface [Windows API],ChangeDefaultTargetRecommendation method, IFhConfigMgr.ChangeDefaultTargetRecommendation, IFhConfigMgr::ChangeDefaultTargetRecommendation, fhcfg/IFhConfigMgr::ChangeDefaultTargetRecommendation, winprog.ifhconfigmgr_changedefaulttargetrecommendation
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
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
 - IFhConfigMgr::ChangeDefaultTargetRecommendation
 - fhcfg/IFhConfigMgr::ChangeDefaultTargetRecommendation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fhcfg.h
api_name:
 - IFhConfigMgr.ChangeDefaultTargetRecommendation
 - FhConfigMgr.ChangeDefaultTargetRecommendation
---

# IFhConfigMgr::ChangeDefaultTargetRecommendation


## -description

Causes the currently assigned backup target to be recommended or not recommended to other members of the home group that the computer belongs to.

> [!NOTE] 
> **IFhConfigMgr** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param Recommend [in]

If set to <b>TRUE</b>, the currently assigned backup target is recommended to other members of the home group. If set to <b>FALSE</b> and the currently assigned backup target is currently recommended to other members of the home group, this recommendation is withdrawn.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code such as one of the values defined in the FhErrors.h header file.

## -remarks

When a backup target is recommended to other computers in the home group, users on those computers see that storage device in the list of available backup targets in the File History item in Control Panel. 

If the backup target is not recommended to other computers in the home group, or if the recommendation is withdrawn, the target does not appear in the list of available backup targets on the other computers.

A backup target cannot be recommended or not recommended on a computer that is joined to a domain or on a computer that is having ARM architecture.

## -see-also

<a href="/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhconfigmgr">IFhConfigMgr</a>