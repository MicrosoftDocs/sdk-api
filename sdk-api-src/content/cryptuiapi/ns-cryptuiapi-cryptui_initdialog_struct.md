---
UID: NS:cryptuiapi.tagCRYPTUI_INITDIALOG_STRUCT
title: CRYPTUI_INITDIALOG_STRUCT (cryptuiapi.h)
description: Supports the CRYPTUI_VIEWCERTIFICATE_STRUCT structure.
helpviewer_keywords: ["*PCRYPTUI_INITDIALOG_STRUCT","CRYPTUI_INITDIALOG_STRUCT","CRYPTUI_INITDIALOG_STRUCT structure [Security]","PCRYPTUI_INITDIALOG_STRUCT","PCRYPTUI_INITDIALOG_STRUCT structure pointer [Security]","cryptuiapi/CRYPTUI_INITDIALOG_STRUCT","cryptuiapi/PCRYPTUI_INITDIALOG_STRUCT","security.cryptui_initdialog_struct"]
old-location: security\cryptui_initdialog_struct.htm
tech.root: security
ms.assetid: c6335c02-3b3e-45e2-bb58-b7213aea500b
ms.date: 12/05/2018
ms.keywords: '*PCRYPTUI_INITDIALOG_STRUCT, CRYPTUI_INITDIALOG_STRUCT, CRYPTUI_INITDIALOG_STRUCT structure [Security], PCRYPTUI_INITDIALOG_STRUCT, PCRYPTUI_INITDIALOG_STRUCT structure pointer [Security], cryptuiapi/CRYPTUI_INITDIALOG_STRUCT, cryptuiapi/PCRYPTUI_INITDIALOG_STRUCT, security.cryptui_initdialog_struct'
req.header: cryptuiapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: CRYPTUI_INITDIALOG_STRUCT, *PCRYPTUI_INITDIALOG_STRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCRYPTUI_INITDIALOG_STRUCT
 - cryptuiapi/tagCRYPTUI_INITDIALOG_STRUCT
 - PCRYPTUI_INITDIALOG_STRUCT
 - cryptuiapi/PCRYPTUI_INITDIALOG_STRUCT
 - CRYPTUI_INITDIALOG_STRUCT
 - cryptuiapi/CRYPTUI_INITDIALOG_STRUCT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cryptuiapi.h
api_name:
 - CRYPTUI_INITDIALOG_STRUCT
---

# CRYPTUI_INITDIALOG_STRUCT structure


## -description

The <b>CRYPTUI_INITDIALOG_STRUCT</b> structure supports the <a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_viewcertificate_structa">CRYPTUI_VIEWCERTIFICATE_STRUCT</a> structure. It  is passed as the <i>lParam</i> in the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> call to each
property sheet that is in the <b>rgPropSheetPages</b> array of the <a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_viewcertificate_structa">CRYPTUI_VIEWCERTIFICATE_STRUCT</a> structure. The <b>CRYPTUI_VIEWCERTIFICATE_STRUCT</b> structure is used in the <a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuidlgviewcertificatea">CryptUIDlgViewCertificate</a> function.

## -struct-fields

### -field lParam

The <b>lParam</b> in the <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> structure.

### -field pCertContext

A pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure for the certificate that <a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuidlgviewcertificatea">CryptUIDlgViewCertificate</a> is displaying.

## -see-also

<a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_viewcertificate_structa">CRYPTUI_VIEWCERTIFICATE_STRUCT</a>



<a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuidlgviewcertificatea">CryptUIDlgViewCertificate</a>