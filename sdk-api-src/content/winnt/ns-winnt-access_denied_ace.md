---
UID: NS:winnt._ACCESS_DENIED_ACE
title: ACCESS_DENIED_ACE (winnt.h)
author: windows-sdk-content
description: Defines an access control entry (ACE) for the discretionary access control list (DACL) that controls access to an object. An access-denied ACE denies access to an object for a specific trustee identified by a security identifier (SID).
old-location: security\access_denied_ace.htm
tech.root: SecAuthZ
ms.assetid: d76a92d0-ccd0-4e73-98b6-43bcd661134d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PACCESS_DENIED_ACE, ACCESS_DENIED_ACE, ACCESS_DENIED_ACE structure [Security], PACCESS_DENIED_ACE, PACCESS_DENIED_ACE structure pointer [Security], _ACCESS_DENIED_ACE, _win32_access_denied_ace_str, security.access_denied_ace, winnt/ACCESS_DENIED_ACE, winnt/PACCESS_DENIED_ACE"
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
 - ACCESS_DENIED_ACE
product: Windows
targetos: Windows
req.typenames: ACCESS_DENIED_ACE
req.redist: 
---

# ACCESS_DENIED_ACE structure


## -description


The <b>ACCESS_DENIED_ACE</b> structure defines an  <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE) for the  <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) that controls access to an object. An access-denied  ACE denies access to an object for a specific <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">trustee</a> identified by a  <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID).
		


## -struct-fields




### -field Header

An <a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a> structure that specifies the size and type of ACE. It also contains flags that control inheritance of the ACE by child objects. The <b>AceType</b> member of the <b>ACE_HEADER</b> structure should be set to ACCESS_DENIED_ACE_TYPE, and the <b>AceSize</b> member should be set to the total number of bytes allocated for the <b>ACCESS_DENIED_ACE</b> structure.


### -field Mask

An 
<a href="https://msdn.microsoft.com/f115ee54-3333-4109-8004-d71904a7a943">ACCESS_MASK</a> structure that specifies the access rights explicitly denied by this ACE.


### -field SidStart

 The first <b>DWORD</b> of a trustee's SID. The remaining bytes of the SID  are stored in contiguous memory after the <b>SidStart</b> member. This SID can be appended with application data.


## -remarks




<a href="https://msdn.microsoft.com/980b8242-2ba2-469f-b834-da7d3fb22e14">ACE structures</a> must be aligned on <b>DWORD</b> boundaries. All Windows memory-management functions return <b>DWORD</b>-aligned handles to memory.

The access rights specified by the <b>Mask</b> member are denied to any <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">trustee</a> that possesses an enabled SID that matches the SID stored in the <b>SidStart</b> member.

An <b>ACCESS_DENIED_ACE</b> structure can be created in an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL) by a call to the <a href="https://msdn.microsoft.com/5b4c4164-48f4-4cd5-b60e-554f2498d547">AddAccessDeniedAce</a> or <a href="https://msdn.microsoft.com/e353c88c-f82e-40c0-b676-38f0060acc81">AddAccessDeniedAceEx</a> function. When these functions are used, the correct amount of memory needed to accommodate the trustee's SID is allocated and the values of the <b>Header.AceType</b> and <b>Header.AceSize</b> members are set automatically. If the <b>AddAccessDeniedAceEx</b> function is used, the <b>Header.AceFlags</b> member is also set. When an <b>ACCESS_DENIED_ACE</b> structure is created outside an ACL, sufficient memory must be allocated to accommodate the complete SID of the trustee in the <b>SidStart</b> member and the contiguous memory following it, and the values of the <b>Header.AceType</b>, <b>Header.AceFlags</b>, and <b>Header.AceSize</b> members must be set explicitly by the application.




## -see-also




<a href="https://msdn.microsoft.com/980b8242-2ba2-469f-b834-da7d3fb22e14">ACE</a>



<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>



<a href="https://msdn.microsoft.com/5b4c4164-48f4-4cd5-b60e-554f2498d547">AddAccessDeniedAce</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>
 

 

