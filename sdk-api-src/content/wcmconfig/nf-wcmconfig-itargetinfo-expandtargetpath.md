---
UID: NF:wcmconfig.ITargetInfo.ExpandTargetPath
title: ITargetInfo::ExpandTargetPath (wcmconfig.h)
description: Expands a location string to indicate the offline installation location. (ITargetInfo.ExpandTargetPath)
helpviewer_keywords: ["ExpandTargetPath","ExpandTargetPath method [SMI]","ExpandTargetPath method [SMI]","ITargetInfo interface","ITargetInfo interface [SMI]","ExpandTargetPath method","ITargetInfo.ExpandTargetPath","ITargetInfo::ExpandTargetPath","smi.itargetinfo_expandtargetpath","wcmconfig/ITargetInfo::ExpandTargetPath"]
old-location: smi\itargetinfo_expandtargetpath.htm
tech.root: SMI
ms.assetid: 7a805c5f-c064-4428-9cfb-1e469450a555
ms.date: 12/05/2018
ms.keywords: ExpandTargetPath, ExpandTargetPath method [SMI], ExpandTargetPath method [SMI],ITargetInfo interface, ITargetInfo interface [SMI],ExpandTargetPath method, ITargetInfo.ExpandTargetPath, ITargetInfo::ExpandTargetPath, smi.itargetinfo_expandtargetpath, wcmconfig/ITargetInfo::ExpandTargetPath
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
 - ITargetInfo::ExpandTargetPath
 - wcmconfig/ITargetInfo::ExpandTargetPath
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
 - ITargetInfo.ExpandTargetPath
---

# ITargetInfo::ExpandTargetPath


## -description

Expands a location string to indicate the offline installation location.

## -parameters

### -param Offline [in]

<b>True</b> if the installation location is offline.

### -param Location [in]

The location string.

### -param ExpandedLocation [out]

The expanded location target path.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. This method may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to return information to the user.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a>
