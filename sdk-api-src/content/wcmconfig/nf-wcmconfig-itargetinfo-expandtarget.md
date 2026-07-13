---
UID: NF:wcmconfig.ITargetInfo.ExpandTarget
title: ITargetInfo::ExpandTarget (wcmconfig.h)
description: Expands a location string to indicate the offline installation location. (ITargetInfo.ExpandTarget)
helpviewer_keywords: ["ExpandTarget","ExpandTarget method [SMI]","ExpandTarget method [SMI]","ITargetInfo interface","ITargetInfo interface [SMI]","ExpandTarget method","ITargetInfo.ExpandTarget","ITargetInfo::ExpandTarget","smi.itargetinfo_expandtarget","wcmconfig/ITargetInfo::ExpandTarget"]
old-location: smi\itargetinfo_expandtarget.htm
tech.root: SMI
ms.assetid: c9c757f4-ad71-42d7-864a-26f3d1e8000b
ms.date: 12/05/2018
ms.keywords: ExpandTarget, ExpandTarget method [SMI], ExpandTarget method [SMI],ITargetInfo interface, ITargetInfo interface [SMI],ExpandTarget method, ITargetInfo.ExpandTarget, ITargetInfo::ExpandTarget, smi.itargetinfo_expandtarget, wcmconfig/ITargetInfo::ExpandTarget
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITargetInfo::ExpandTarget
 - wcmconfig/ITargetInfo::ExpandTarget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ITargetInfo.ExpandTarget
---

# ITargetInfo::ExpandTarget


## -description

Expands a location string to indicate the offline installation location.

## -parameters

### -param Offline [in]

<b>True</b> if the installation location is offline.

### -param Location [in]

The location string.

### -param ExpandedLocation [out]

The expanded location string.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. This method may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to return information to the user.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a>
