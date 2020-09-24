---
UID: NF:xenroll.ICEnroll4.setPendingRequestInfo
title: ICEnroll4::setPendingRequestInfo (xenroll.h)
description: Sets properties for a pending request. This method was first defined in the ICEnroll4 interface.
helpviewer_keywords: ["CEnroll object [Security]","setPendingRequestInfo method","ICEnroll4 interface [Security]","setPendingRequestInfo method","ICEnroll4.setPendingRequestInfo","ICEnroll4::setPendingRequestInfo","_xen_icenroll4_setpendingrequestinfo","security.icenroll4_setpendingrequestinfo","setPendingRequestInfo","setPendingRequestInfo method [Security]","setPendingRequestInfo method [Security]","CEnroll object","setPendingRequestInfo method [Security]","ICEnroll4 interface","xenroll/ICEnroll4::setPendingRequestInfo"]
old-location: security\icenroll4_setpendingrequestinfo.htm
tech.root: security
ms.assetid: be369059-5852-4cde-8f78-d5883735b670
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],setPendingRequestInfo method, ICEnroll4 interface [Security],setPendingRequestInfo method, ICEnroll4.setPendingRequestInfo, ICEnroll4::setPendingRequestInfo, _xen_icenroll4_setpendingrequestinfo, security.icenroll4_setpendingrequestinfo, setPendingRequestInfo, setPendingRequestInfo method [Security], setPendingRequestInfo method [Security],CEnroll object, setPendingRequestInfo method [Security],ICEnroll4 interface, xenroll/ICEnroll4::setPendingRequestInfo
req.header: xenroll.h
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICEnroll4::setPendingRequestInfo
 - xenroll/ICEnroll4::setPendingRequestInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.setPendingRequestInfo
 - CEnroll.setPendingRequestInfo
---

# ICEnroll4::setPendingRequestInfo


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>setPendingRequestInfo</b> method sets properties for a pending request. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

## -parameters

### -param lRequestID [in]

An identifier for the request, as assigned by the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>.

### -param strCADNS [in]

The Domain Name System (DNS) name of the certification authority. The  <i>strCADNS</i> parameter cannot be <b>NULL</b>.

### -param strCAName [in]

The name of the certification authority. The <i>strCAName</i> parameter cannot be <b>NULL</b>.

### -param strFriendlyName [in]

The display name of the certification authority. The <i>strFriendlyName</i> parameter can be <b>NULL</b>.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.