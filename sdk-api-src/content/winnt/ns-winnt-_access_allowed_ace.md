---
UID: NS:winnt._ACCESS_ALLOWED_ACE
title: "_ACCESS_ALLOWED_ACE"
author: windows-driver-content
description: Defines an access control entry (ACE) for the discretionary access control list (DACL) that controls access to an object. An access-allowed ACE allows access to an object for a specific trustee identified by a security identifier (SID).
old-location: security\access_allowed_ace.htm
old-project: SecAuthZ
ms.assetid: 002a3fa7-02a3-4832-948e-b048f5f5818f
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: "*PACCESS_ALLOWED_ACE, ACCESS_ALLOWED_ACE, ACCESS_ALLOWED_ACE structure [Security], PACCESS_ALLOWED_ACE, PACCESS_ALLOWED_ACE structure pointer [Security], _ACCESS_ALLOWED_ACE, _win32_access_allowed_ace_str, security.access_allowed_ace, winnt/ACCESS_ALLOWED_ACE, winnt/PACCESS_ALLOWED_ACE"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ACCESS_ALLOWED_ACE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnt.h
api_name:
-	ACCESS_ALLOWED_ACE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _ACCESS_ALLOWED_ACE structure


## -description



			The <b>ACCESS_ALLOWED_ACE</b> structure defines an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE) for the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) that controls access to an object. An access-allowed ACE allows access to an object for a specific <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">trustee</a> identified by a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID).
		


## -struct-fields




### -field Header


<a href="https://msdn.microsoft.com/library/windows/hardware/ff538847">ACE_HEADER</a> structure that specifies the size and type of ACE. It also contains flags that control inheritance of the ACE by child objects. The <b>AceType</b> member of the <b>ACE_HEADER</b> structure should be set to ACCESS_ALLOWED_ACE_TYPE, and the <b>AceSize</b> member should be set to the total number of bytes allocated for the <b>ACCESS_ALLOWED_ACE</b> structure.


### -field Mask

Specifies an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a> structure that specifies the access rights granted by this ACE.


### -field SidStart

The first <b>DWORD</b> of a trustee's SID. The remaining bytes of the SID  are stored in contiguous memory after the <b>SidStart</b> member. This SID can be appended with application data.


## -remarks



ACE structures must be aligned on <b>DWORD</b> boundaries. All Windows memory-management functions return <b>DWORD</b>-aligned handles to memory.

The access rights specified by the <b>Mask</b> member are granted to any <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">trustee</a> that possesses an enabled SID that matches the SID stored in the <b>SidStart</b> member.

An <b>ACCESS_ALLOWED_ACE</b> structure can be created in an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL) by a call to the <a href="https://msdn.microsoft.com/1004353a-f907-4452-9c0f-85eba0ece813">AddAccessAllowedAce</a> or <a href="https://msdn.microsoft.com/6ddec01f-237f-4b6a-8ea8-a126017b30c5">AddAccessAllowedAceEx</a> function. When these functions are used, the correct amount of memory needed to accommodate the trustee's SID is allocated and the values of the <b>Header.AceType</b> and <b>Header.AceSize</b> members are set automatically. If the <b>AddAccessAllowedAceEx</b> function is used, the <b>Header.AceFlags</b> member is also set. When an <b>ACCESS_ALLOWED_ACE</b> structure is created outside an ACL, sufficient memory must be allocated to accommodate the complete SID of the trustee in the <b>SidStart</b> member and the contiguous memory following it, and the values of the <b>Header.AceType</b>, <b>Header.AceFlags</b>, and <b>Header.AceSize</b> members must be set explicitly by the application.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538844">ACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a>



<a href="https://msdn.microsoft.com/1004353a-f907-4452-9c0f-85eba0ece813">AddAccessAllowedAce</a>



<a href="https://msdn.microsoft.com/f472d864-a273-49b5-b5e2-98772989971e">AddAce</a>



<a href="https://msdn.microsoft.com/5b5d8751-20d7-40a2-bd70-cfbe956aaa03">GetAce</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>
 

 

