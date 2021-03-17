---
UID: NS:sspi._SecPkgContext_SubjectAttributes
title: SecPkgContext_SubjectAttributes (sspi.h)
description: Returns the security attribute information.
helpviewer_keywords: ["*PSecPkgContext_SubjectAttributes","PSecPkgContext_SubjectAttributes","PSecPkgContext_SubjectAttributes structure pointer [Security]","SecPkgContext_SubjectAttributes","SecPkgContext_SubjectAttributes structure [Security]","security.secpkgcontext_subjectattributes","sspi/PSecPkgContext_SubjectAttributes","sspi/SecPkgContext_SubjectAttributes"]
old-location: security\secpkgcontext_subjectattributes.htm
tech.root: security
ms.assetid: 548E972F-EB94-4BBD-94F2-FA38184D179A
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_SubjectAttributes, PSecPkgContext_SubjectAttributes, PSecPkgContext_SubjectAttributes structure pointer [Security], SecPkgContext_SubjectAttributes, SecPkgContext_SubjectAttributes structure [Security], security.secpkgcontext_subjectattributes, sspi/PSecPkgContext_SubjectAttributes, sspi/SecPkgContext_SubjectAttributes'
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SecPkgContext_SubjectAttributes, *PSecPkgContext_SubjectAttributes
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_SubjectAttributes
 - sspi/_SecPkgContext_SubjectAttributes
 - PSecPkgContext_SubjectAttributes
 - sspi/PSecPkgContext_SubjectAttributes
 - SecPkgContext_SubjectAttributes
 - sspi/SecPkgContext_SubjectAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SecPkgContext_SubjectAttributes
---

# SecPkgContext_SubjectAttributes structure


## -description

The <b>SecPkgContext_SubjectAttributes</b> structure returns the security attribute information.

## -struct-fields

### -field AttributeInfo

Pointer to a <b>void</b> that receives the attribute information stored in a <a href="/windows/desktop/api/authz/ns-authz-authz_security_attributes_information">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a> structure.