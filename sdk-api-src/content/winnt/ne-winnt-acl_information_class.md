---
UID: NE:winnt._ACL_INFORMATION_CLASS
title: ACL_INFORMATION_CLASS (winnt.h)
description: Contains values that specify the type of information being assigned to or retrieved from an access control list (ACL).
helpviewer_keywords: ["ACL_INFORMATION_CLASS","ACL_INFORMATION_CLASS enumeration [Security]","AclRevisionInformation","AclSizeInformation","_win32_acl_information_class_str","security.acl_information_class","winnt/ACL_INFORMATION_CLASS","winnt/AclRevisionInformation","winnt/AclSizeInformation"]
old-location: security\acl_information_class.htm
tech.root: security
ms.assetid: e1abf877-9757-4ee4-b7da-f3e7eb53bddd
ms.date: 12/05/2018
ms.keywords: ACL_INFORMATION_CLASS, ACL_INFORMATION_CLASS enumeration [Security], AclRevisionInformation, AclSizeInformation, _win32_acl_information_class_str, security.acl_information_class, winnt/ACL_INFORMATION_CLASS, winnt/AclRevisionInformation, winnt/AclSizeInformation
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
req.typenames: ACL_INFORMATION_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACL_INFORMATION_CLASS
 - winnt/_ACL_INFORMATION_CLASS
 - ACL_INFORMATION_CLASS
 - winnt/ACL_INFORMATION_CLASS
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
 - ACL_INFORMATION_CLASS
---

# ACL_INFORMATION_CLASS enumeration


## -description

The <b>ACL_INFORMATION_CLASS</b> enumeration contains values that specify the type of information being assigned to or retrieved from an <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL).

## -enum-fields

### -field AclRevisionInformation:1

Indicates ACL revision information.

### -field AclSizeInformation

Indicates ACL size information.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl_revision_information">ACL_REVISION_INFORMATION</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl_size_information">ACL_SIZE_INFORMATION</a>



<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-enumerations">Authorization Enumerations</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getaclinformation">GetAclInformation</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setaclinformation">SetAclInformation</a>
