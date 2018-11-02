---
UID: NS:winnt._ACL_SIZE_INFORMATION
title: "_ACL_SIZE_INFORMATION"
author: windows-sdk-content
description: Contains information about the size of an ACL structure.
old-location: security\acl_size_information.htm
tech.root: secauthz
ms.assetid: 05034096-211d-4ee3-a686-dfebfa167814
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PACL_SIZE_INFORMATION, ACL_SIZE_INFORMATION, ACL_SIZE_INFORMATION structure [Security], PACL_SIZE_INFORMATION, PACL_SIZE_INFORMATION structure pointer [Security], _ACL_SIZE_INFORMATION, _win32_acl_size_information_str, security.acl_size_information, winnt/ACL_SIZE_INFORMATION, winnt/PACL_SIZE_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - ACL_SIZE_INFORMATION
product: Windows
targetos: Windows
req.typenames: ACL_SIZE_INFORMATION
req.redist: 
---

# _ACL_SIZE_INFORMATION structure


## -description


The <b>ACL_SIZE_INFORMATION</b> structure contains information about the size of an <a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> structure.


## -struct-fields




### -field AceCount

The number of <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) in the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL).


### -field AclBytesInUse

The number of bytes in the ACL actually used to store the ACEs and <a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> structure. This may be less than the total number of bytes allocated to the ACL.


### -field AclBytesFree

The number of unused bytes in the ACL.


## -see-also




<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>



<a href="https://msdn.microsoft.com/e1abf877-9757-4ee4-b7da-f3e7eb53bddd">ACL_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/cdc7f6b1-aaa1-4893-a192-5a42233b3ec1">ACL_REVISION_INFORMATION</a>



<a href="https://msdn.microsoft.com/23ef6abd-03e9-439e-ba05-629c8d61cd66">GetAclInformation</a>



<a href="https://msdn.microsoft.com/bb4dd7f9-2f15-4a27-89c9-1675f4fb8d92">SetAclInformation</a>
 

 

