---
UID: NS:slpublic._tagSL_AD_ACTIVATION_INFO
title: SL_AD_ACTIVATION_INFO (slpublic.h)
description: Specifies information used for the retail or Active Directory phone activation of a license.
helpviewer_keywords: ["PSL_AD_ACTIVATION_INFO","PSL_AD_ACTIVATION_INFO structure pointer [Security]","SL_AD_ACTIVATION_INFO","SL_AD_ACTIVATION_INFO structure [Security]","security.sl_ad_activation_info","slpublic/PSL_AD_ACTIVATION_INFO","slpublic/SL_AD_ACTIVATION_INFO"]
old-location: security\sl_ad_activation_info.htm
tech.root: security
ms.assetid: 17012938-3E59-47DA-A046-8264CC3F06AF
ms.date: 12/05/2018
ms.keywords: PSL_AD_ACTIVATION_INFO, PSL_AD_ACTIVATION_INFO structure pointer [Security], SL_AD_ACTIVATION_INFO, SL_AD_ACTIVATION_INFO structure [Security], security.sl_ad_activation_info, slpublic/PSL_AD_ACTIVATION_INFO, slpublic/SL_AD_ACTIVATION_INFO
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SL_AD_ACTIVATION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagSL_AD_ACTIVATION_INFO
 - slpublic/_tagSL_AD_ACTIVATION_INFO
 - SL_AD_ACTIVATION_INFO
 - slpublic/SL_AD_ACTIVATION_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - slpublic.h
api_name:
 - SL_AD_ACTIVATION_INFO
---

# SL_AD_ACTIVATION_INFO structure


## -description

Specifies information used for the retail or Active Directory phone activation of a license.

## -struct-fields

### -field header

 An <a href="/windows/desktop/api/slpublic/ns-slpublic-sl_activation_info_header">SL_ACTIVATION_INFO_HEADER</a> structure that contains the activation type.  The activation type determines whether the <b>SL_AD_ACTIVATION_INFO</b> structure is used for retail or Active Directory phone activation.

### -field pwszProductKey

The product key.

### -field pwszActivationObjectName

The name of the activation object.

## -remarks

For an example of how this structure is used, see the description of the <i>pActivationInfo</i> parameter in the <a href="/windows/desktop/api/slpublic/nf-slpublic-slactivateproduct">SLActivateProduct</a>, <a href="/windows/desktop/api/slpublic/nf-slpublic-sldepositofflineconfirmationidex">SLDepositOfflineConfirmationIdEx</a>, and <a href="/windows/desktop/api/slpublic/nf-slpublic-slgenerateofflineinstallationidex">SLGenerateOfflineInstallationIdEx</a>  functions.

## -see-also

<a href="/windows/desktop/api/slpublic/nf-slpublic-slactivateproduct">SLActivateProduct</a>



<a href="/windows/desktop/api/slpublic/nf-slpublic-sldepositofflineconfirmationidex">SLDepositOfflineConfirmationIdEx</a>



<a href="/windows/desktop/api/slpublic/nf-slpublic-slgenerateofflineinstallationidex">SLGenerateOfflineInstallationIdEx</a>



<a href="/windows/desktop/api/slpublic/ns-slpublic-sl_activation_info_header">SL_ACTIVATION_INFO_HEADER</a>



<a href="/windows/desktop/api/slpublic/ne-slpublic-sl_activation_type">SL_ACTIVATION_TYPE</a>