---
UID: NF:certenroll.ICspStatus.get_Ordinal
title: ICspStatus::get_Ordinal (certenroll.h)
description: Specifies or retrieves the position of the ICspStatus object in the ICspStatuses collection. (Get)
helpviewer_keywords: ["ICspStatus interface [Security]","Ordinal property","ICspStatus.Ordinal","ICspStatus.get_Ordinal","ICspStatus::Ordinal","ICspStatus::get_Ordinal","ICspStatus::put_Ordinal","Ordinal property [Security]","Ordinal property [Security]","ICspStatus interface","certenroll/ICspStatus::Ordinal","certenroll/ICspStatus::get_Ordinal","certenroll/ICspStatus::put_Ordinal","get_Ordinal","security.icspstatus_ordinal_property"]
old-location: security\icspstatus_ordinal_property.htm
tech.root: security
ms.assetid: e392e28f-084e-43a7-8a5e-14bea0ed8d58
ms.date: 12/05/2018
ms.keywords: ICspStatus interface [Security],Ordinal property, ICspStatus.Ordinal, ICspStatus.get_Ordinal, ICspStatus::Ordinal, ICspStatus::get_Ordinal, ICspStatus::put_Ordinal, Ordinal property [Security], Ordinal property [Security],ICspStatus interface, certenroll/ICspStatus::Ordinal, certenroll/ICspStatus::get_Ordinal, certenroll/ICspStatus::put_Ordinal, get_Ordinal, security.icspstatus_ordinal_property
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICspStatus::get_Ordinal
 - certenroll/ICspStatus::get_Ordinal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspStatus.Ordinal
 - ICspStatus.get_Ordinal
 - ICspStatus.put_Ordinal
---

# ICspStatus::get_Ordinal


## -description

The <b>Ordinal</b> property specifies or retrieves the  position of the <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object in the <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a> collection.

This property is read/write.

## -parameters

## -remarks

To iterate through the <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a> collection by ordinal, call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspstatuses-get_itembyordinal">ItemByOrdinal</a> property. The ordinal order of the <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> objects in the collection can vary each time the collection is enumerated for a variety of reasons including, but not limited to, the following:<ul>
<li>Certificate request template settings</li>
<li>Property values for the cryptographic provider</li>
<li>Private key property values</li>
</ul>


For example, assume that the version 2 template chosen to create a certificate request specifies that the certificate can only be used for signing (the <b>pKIDefaultKeySpec</b> template attribute is XCN_AT_SIGNATURE) and that the default provider is the Microsoft Enhanced RSA and AES Cryptographic Provider. Notice that the template restricts the certificate to signing even though the provider supports both encryption and signing algorithms. That is, the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_keyspec">KeySpec</a> property on the provider is a bitwise combination of the XCN_AT_KEYEXCHANGE and XCN_AT_SIGNATURE constants, but the <b>pKIDefaultKeySpec</b> template attribute supports only XCN_AT_SIGNATURE.

The <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> objects in the collection will be ordered in the following manner:<ul>
<li>Of the <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> objects enumerated for this provider, those associated with signature algorithms (XCN_AT_SIGNATURE) are ordered first (lower ordinal value) and their <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_display">Display</a> and <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_selected">Selected</a> properties are enabled. <div class="alert"><b>Note</b>  If the  <b>pKIDefaultKeySpec</b> template attribute had been XCN_AT_KEYEXCHANGE, the encryption algorithms would be ordered first.</div>
<div> </div>
</li>
<li>Of the <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> objects enumerated for this provider, those associated with encryption algorithms (XCN_AT_KEYEXCHANGE) are ordered later (higher ordinal values) and their <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_display">Display</a> and <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_selected">Selected</a> properties are not enabled.</li>
<li>For all other installed CryptoAPI providers that support asymmetric signing algorithms (XCN_AT_SIGNATURE) but which are not associated with the specified provider, the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_display">Display</a> property is enabled and the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_selected">Selected</a> property is not enabled.</li>
<li>For all other installed CryptoAPI providers that support asymmetric encryption algorithms (XCN_AT_KEYEXCHANGE), the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_display">Display</a> and <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_selected">Selected</a> properties are not enabled.</li>
<li>For all installed Cryptography API: Next Generation (CNG) providers, the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_display">Display</a> and <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_selected">Selected</a> properties are not enabled.</li>
</ul>


For another example, assume that a version 3 template specifies one specific CNG provider and  algorithm. That provider/algorithm pair (<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object) is ordered first, enabled for display and selected. All other algorithms supported by that provider are ordered later, not enabled for display, and not selected. All other providers that support the specified algorithm will be ordered later still, enabled for display, but not selected. All remaining provider/algorithm pairs will not be enabled for display and not selected.<div class="alert"><b>Note</b>  CNG providers do not support the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_keyspec">KeySpec</a> intended use concept. They return XCN_AT_NONE for this property value.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a>
