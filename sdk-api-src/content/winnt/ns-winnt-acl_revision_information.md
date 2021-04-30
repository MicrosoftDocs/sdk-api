---
UID: NS:winnt._ACL_REVISION_INFORMATION
title: ACL_REVISION_INFORMATION (winnt.h)
description: Contains revision information about an ACL structure.
helpviewer_keywords: ["*PACL_REVISION_INFORMATION","ACL_REVISION_INFORMATION","ACL_REVISION_INFORMATION structure [Security]","PACL_REVISION_INFORMATION","PACL_REVISION_INFORMATION structure pointer [Security]","_ACL_REVISION_INFORMATION","_win32_acl_revision_information_str","security.acl_revision_information","winnt/ACL_REVISION_INFORMATION","winnt/PACL_REVISION_INFORMATION"]
old-location: security\acl_revision_information.htm
tech.root: security
ms.assetid: cdc7f6b1-aaa1-4893-a192-5a42233b3ec1
ms.date: 12/05/2018
ms.keywords: '*PACL_REVISION_INFORMATION, ACL_REVISION_INFORMATION, ACL_REVISION_INFORMATION structure [Security], PACL_REVISION_INFORMATION, PACL_REVISION_INFORMATION structure pointer [Security], _ACL_REVISION_INFORMATION, _win32_acl_revision_information_str, security.acl_revision_information, winnt/ACL_REVISION_INFORMATION, winnt/PACL_REVISION_INFORMATION'
req.header: winnt.h
req.include-header: Windows.h
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
req.typenames: ACL_REVISION_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACL_REVISION_INFORMATION
 - winnt/_ACL_REVISION_INFORMATION
 - ACL_REVISION_INFORMATION
 - winnt/ACL_REVISION_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - ACL_REVISION_INFORMATION
---

# ACL_REVISION_INFORMATION structure


## -description

The <b>ACL_REVISION_INFORMATION</b> structure contains revision information about an <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure.

## -struct-fields

### -field AclRevision

Specifies a revision number. The current revision number is ACL_REVISION.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/api/winnt/ne-winnt-acl_information_class">ACL_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl_size_information">ACL_SIZE_INFORMATION</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getaclinformation">GetAclInformation</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setaclinformation">SetAclInformation</a>