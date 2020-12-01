---
UID: NF:xenroll.ICEnroll4.addExtensionToRequest
title: ICEnroll4::addExtensionToRequest (xenroll.h)
description: The ICEnroll4::addExtensionToRequest method adds an extension to the request.
helpviewer_keywords: ["CEnroll object [Security]","addExtensionToRequest method","ICEnroll4 interface [Security]","addExtensionToRequest method","ICEnroll4.addExtensionToRequest","ICEnroll4::addExtensionToRequest","_xen_icenroll4_addextensiontorequest","addExtensionToRequest","addExtensionToRequest method [Security]","addExtensionToRequest method [Security]","CEnroll object","addExtensionToRequest method [Security]","ICEnroll4 interface","security.icenroll4_addextensiontorequest","xenroll/ICEnroll4::addExtensionToRequest"]
old-location: security\icenroll4_addextensiontorequest.htm
tech.root: security
ms.assetid: 0bd46cd6-cc7e-4d87-b8ff-8fa01f639282
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],addExtensionToRequest method, ICEnroll4 interface [Security],addExtensionToRequest method, ICEnroll4.addExtensionToRequest, ICEnroll4::addExtensionToRequest, _xen_icenroll4_addextensiontorequest, addExtensionToRequest, addExtensionToRequest method [Security], addExtensionToRequest method [Security],CEnroll object, addExtensionToRequest method [Security],ICEnroll4 interface, security.icenroll4_addextensiontorequest, xenroll/ICEnroll4::addExtensionToRequest
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
 - ICEnroll4::addExtensionToRequest
 - xenroll/ICEnroll4::addExtensionToRequest
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
 - ICEnroll4.addExtensionToRequest
 - CEnroll.addExtensionToRequest
---

# ICEnroll4::addExtensionToRequest


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addExtensionToRequest</b> method adds an extension to the request. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

## -parameters

### -param Flags [in]

Specifies whether the extension is critical. 
If <b>TRUE</b>, the extension being added is critical. If <b>FALSE</b>, it is not critical.

Note that <b>TRUE</b> is defined (in a Microsoft header file) for C/C++ programmers as one, while  Visual Basic defines the <b>True</b> keyword as negative one. As a result, Visual Basic developers must use one (instead of <b>True</b>) to set this parameter to <b>TRUE</b>. However, to set this parameter to <b>FALSE</b>, Visual Basic developers can use zero or <b>False</b>.

### -param strName [in]

The <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) that represents the extension name.

### -param strValue [in]

The base64-encoded or binary extension value.

## -returns

<h3>VB</h3>
The return value is an <b>HRESULT</b>, with <b>S_OK</b> returned if the call is successful.