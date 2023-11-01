---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.SetPolicy
title: IXpsSigningOptions::SetPolicy (xpsdigitalsignature.h)
description: Sets the XPS_SIGN_POLICY value that represents the signing policy.
helpviewer_keywords: ["IXpsSigningOptions interface [XPS Documents and Packaging]","SetPolicy method","IXpsSigningOptions.SetPolicy","IXpsSigningOptions::SetPolicy","SetPolicy","SetPolicy method [XPS Documents and Packaging]","SetPolicy method [XPS Documents and Packaging]","IXpsSigningOptions interface","xps.ixpssigningoptions_setpolicy","xpsdigitalsignature/IXpsSigningOptions::SetPolicy"]
old-location: xps\ixpssigningoptions_setpolicy.htm
tech.root: xps
ms.assetid: 6e1738b3-f1ce-407e-bbaa-7f4c57e30028
ms.date: 12/05/2018
ms.keywords: IXpsSigningOptions interface [XPS Documents and Packaging],SetPolicy method, IXpsSigningOptions.SetPolicy, IXpsSigningOptions::SetPolicy, SetPolicy, SetPolicy method [XPS Documents and Packaging], SetPolicy method [XPS Documents and Packaging],IXpsSigningOptions interface, xps.ixpssigningoptions_setpolicy, xpsdigitalsignature/IXpsSigningOptions::SetPolicy
req.header: xpsdigitalsignature.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsDigitalSignature.idl
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
 - IXpsSigningOptions::SetPolicy
 - xpsdigitalsignature/IXpsSigningOptions::SetPolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSigningOptions.SetPolicy
---

# IXpsSigningOptions::SetPolicy


## -description

Sets the <a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy">XPS_SIGN_POLICY</a> value that represents the signing policy.

## -parameters

### -param policy [in]

The logical <b>OR</b> of  the <a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy">XPS_SIGN_POLICY</a> values to be set as the signing policy.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If an <a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy">XPS_SIGN_POLICY</a> value is set and it does not have a  corresponding part in the package being signed, only the  relationship type will be signed.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy">XPS_SIGN_POLICY</a>