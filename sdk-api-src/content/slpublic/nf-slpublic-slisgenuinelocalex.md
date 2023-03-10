---
UID: NF:slpublic.SLIsGenuineLocalEx
title: SLIsGenuineLocalEx function (slpublic.h)
description: Checks whether the specified application installation is genuine.
helpviewer_keywords: ["SLIsGenuineLocalEx","SLIsGenuineLocalEx function [Security]","security.slisgenuinelocalex","slpublic/SLIsGenuineLocalEx"]
old-location: security\slisgenuinelocalex.htm
tech.root: security
ms.assetid: 171edde8-edbd-4040-9623-359f13817687
ms.date: 12/05/2018
ms.keywords: SLIsGenuineLocalEx, SLIsGenuineLocalEx function [Security], security.slisgenuinelocalex, slpublic/SLIsGenuineLocalEx
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Slwga.lib
req.dll: Slwga.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SLIsGenuineLocalEx
 - slpublic/SLIsGenuineLocalEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Slwga.dll
api_name:
 - SLIsGenuineLocalEx
---

# SLIsGenuineLocalEx function


## -description

Checks whether the specified application installation is genuine.

## -parameters

### -param pAppId [in]

A pointer to an <b>SLID</b> structure that specifies the application to check.

### -param pSkuId [in, optional]

A pointer to an <b>SLID</b> structure that specifies the SKU of the application to check.

If this parameter is not <b>NULL</b>, this function uses the value of this parameter instead of the value of the <i>pAppId</i> parameter to check whether the application installation is genuine. If the SKU license contains a <b>ProductUniquenessGroupId</b>  value, that value is also used to check whether the application is genuine.

### -param pGenuineState [out]

A pointer to a value of the <a href="/windows/desktop/api/slpublic/ne-slpublic-sl_genuine_state">SL_GENUINE_STATE</a> enumeration that specifies the state of the installation.  This function does not change the value of this parameter if the return value is any value other than <b>S_OK</b>.

If this parameter is <b>NULL</b>, the function fails with a return value of <b>E_INVALIDARG</b>.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function checks the <b>Tampered</b> flag of the license associated with the specified application and the SKU, if specified. If the license is not valid, or if the <b>Tampered</b> flag of either license is set, the installation is not considered genuine.