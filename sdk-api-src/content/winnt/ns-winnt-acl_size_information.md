---
UID: NS:winnt._ACL_SIZE_INFORMATION
title: ACL_SIZE_INFORMATION (winnt.h)
description: Contains information about the size of an ACL structure.
helpviewer_keywords: ["*PACL_SIZE_INFORMATION","ACL_SIZE_INFORMATION","ACL_SIZE_INFORMATION structure [Security]","PACL_SIZE_INFORMATION","PACL_SIZE_INFORMATION structure pointer [Security]","_ACL_SIZE_INFORMATION","_win32_acl_size_information_str","security.acl_size_information","winnt/ACL_SIZE_INFORMATION","winnt/PACL_SIZE_INFORMATION"]
old-location: security\acl_size_information.htm
tech.root: security
ms.assetid: 05034096-211d-4ee3-a686-dfebfa167814
ms.date: 12/05/2018
ms.keywords: '*PACL_SIZE_INFORMATION, ACL_SIZE_INFORMATION, ACL_SIZE_INFORMATION structure [Security], PACL_SIZE_INFORMATION, PACL_SIZE_INFORMATION structure pointer [Security], _ACL_SIZE_INFORMATION, _win32_acl_size_information_str, security.acl_size_information, winnt/ACL_SIZE_INFORMATION, winnt/PACL_SIZE_INFORMATION'
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
req.typenames: ACL_SIZE_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACL_SIZE_INFORMATION
 - winnt/_ACL_SIZE_INFORMATION
 - ACL_SIZE_INFORMATION
 - winnt/ACL_SIZE_INFORMATION
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
 - ACL_SIZE_INFORMATION
---

# ACL_SIZE_INFORMATION structure


## -description

The <b>ACL_SIZE_INFORMATION</b> structure contains information about the size of an <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure.

## -struct-fields

### -field AceCount

The number of <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) in the <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL).

### -field AclBytesInUse

The number of bytes in the ACL actually used to store the ACEs and <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure. This may be less than the total number of bytes allocated to the ACL.

### -field AclBytesFree

The number of unused bytes in the ACL.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/api/winnt/ne-winnt-acl_information_class">ACL_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl_revision_information">ACL_REVISION_INFORMATION</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getaclinformation">GetAclInformation</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setaclinformation">SetAclInformation</a>