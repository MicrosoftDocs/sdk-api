---
UID: NF:wcmconfig.ITargetInfo.GetEnumerator
title: ITargetInfo::GetEnumerator (wcmconfig.h)
description: Gets the enumerator used to access the collection of offline properties.
helpviewer_keywords: ["GetEnumerator","GetEnumerator method [SMI]","GetEnumerator method [SMI]","ITargetInfo interface","ITargetInfo interface [SMI]","GetEnumerator method","ITargetInfo.GetEnumerator","ITargetInfo::GetEnumerator","smi.itargetinfo_getenumerator","wcmconfig/ITargetInfo::GetEnumerator"]
old-location: smi\itargetinfo_getenumerator.htm
tech.root: SMI
ms.assetid: 2e7854dd-93eb-4626-a67d-4bd3dd79a75b
ms.date: 12/05/2018
ms.keywords: GetEnumerator, GetEnumerator method [SMI], GetEnumerator method [SMI],ITargetInfo interface, ITargetInfo interface [SMI],GetEnumerator method, ITargetInfo.GetEnumerator, ITargetInfo::GetEnumerator, smi.itargetinfo_getenumerator, wcmconfig/ITargetInfo::GetEnumerator
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
 - ITargetInfo::GetEnumerator
 - wcmconfig/ITargetInfo::GetEnumerator
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
 - ITargetInfo.GetEnumerator
---

# ITargetInfo::GetEnumerator


## -description

Gets the enumerator used to access the collection of offline properties.

## -parameters

### -param Enumerator [out]

A pointer to an  <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-iitemenumerator">IItemEnumerator</a> object that provides access to  the collection of offline properties.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -remarks

<div class="alert"><b>Note</b>   This method is not implemented.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a>