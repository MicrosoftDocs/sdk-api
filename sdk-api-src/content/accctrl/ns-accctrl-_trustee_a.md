---
UID: NS:accctrl._TRUSTEE_A
title: "_TRUSTEE_A"
author: windows-sdk-content
description: Identifies the user account, group account, or logon session to which an access control entry (ACE) applies.
old-location: security\trustee.htm
old-project: SecAuthZ
ms.assetid: 120e93eb-680f-4f86-879d-bc2de10d4641
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: "*PTRUSTEEA, *PTRUSTEE_A, PTRUSTEE, PTRUSTEE structure pointer [Security], TRUSTEE, TRUSTEE structure [Security], TRUSTEEA, TRUSTEE_, TRUSTEE_A, TRUSTEE_IS_NAME, TRUSTEE_IS_OBJECTS_AND_NAME, TRUSTEE_IS_OBJECTS_AND_SID, TRUSTEE_IS_SID, TRUSTEE_W, _TRUSTEE_A, _win32_trustee_str, accctrl/PTRUSTEE, accctrl/TRUSTEE, accctrl/TRUSTEE_A, accctrl/TRUSTEE_W, security.trustee"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: accctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TRUSTEE_W (Unicode) and TRUSTEE_A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRUSTEE_A, *PTRUSTEE_A, TRUSTEEA, *PTRUSTEEA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AccCtrl.h
api_name:
 - TRUSTEE
 - TRUSTEE_A
 - TRUSTEE_W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
---

# _TRUSTEE_A structure


## -description


The <b>TRUSTEE</b> structure identifies the user account, group account, or <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a> to which an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE) applies. The structure can use a name or a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) to identify the trustee.

Access control functions, such as 
<a href="https://msdn.microsoft.com/05960fc1-1ad2-4c19-a65c-62259af5e18c">SetEntriesInAcl</a> and 
<a href="https://msdn.microsoft.com/186aa6aa-efc3-4f8a-acad-e257da3dac0b">GetExplicitEntriesFromAcl</a>, use this structure to identify the logon account associated with the access control or audit control information in an <a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structure.


## -struct-fields




### -field pMultipleTrustee

A pointer to a <b>TRUSTEE</b> structure that identifies a server account that can impersonate the user identified by the <b>ptstrName</b> member. This member is not currently supported and must be <b>NULL</b>.


### -field MultipleTrusteeOperation

A value of the 
<a href="https://msdn.microsoft.com/00b00678-5c87-4aa9-8232-5f0f1cb48e24">MULTIPLE_TRUSTEE_OPERATION</a> enumeration type. Currently, this member must be NO_MULTIPLE_TRUSTEE.


### -field TrusteeForm

A value from the 
<a href="https://msdn.microsoft.com/991ac6cb-3fc9-4915-b5c9-ae73efb25d68">TRUSTEE_FORM</a> enumeration type that indicates the type of data pointed to by the <b>ptstrName</b> member.


### -field TrusteeType

A value from the 
<a href="https://msdn.microsoft.com/6519c79d-9cee-4565-a71e-0b81a27c1185">TRUSTEE_TYPE</a> enumeration type that indicates whether the trustee is a user account, a group account, or an unknown account type.


### -field ptstrName.case

 


### -field ptstrName.case.TRUSTEE_IS_NAME

 


### -field pSid

 


### -field pSid.case

 


### -field pSid.case.TRUSTEE_IS_SID

 


### -field pObjectsAndSid

 


### -field pObjectsAndSid.case

 


### -field pObjectsAndSid.case.TRUSTEE_IS_OBJECTS_AND_SID

 


### -field pObjectsAndName

 


### -field pObjectsAndName.case

 


### -field pObjectsAndName.case.TRUSTEE_IS_OBJECTS_AND_NAME

 


### -field switch_is

 


### -field switch_is.TrusteeForm

 


### -field ptstrName

 A pointer to a buffer that identifies the trustee and, optionally, contains information about object-specific ACEs. The type of data depends on the value of the <b>TrusteeForm</b> member. 



This member can be one of the following values.
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUSTEE_IS_NAME"></a><a id="trustee_is_name"></a><dl>
<dt><b>TRUSTEE_IS_NAME</b></dt>
</dl>
</td>
<td width="60%">
A pointer to a <b>null</b>-terminated string that contains the name of the trustee.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUSTEE_IS_OBJECTS_AND_NAME"></a><a id="trustee_is_objects_and_name"></a><dl>
<dt><b>TRUSTEE_IS_OBJECTS_AND_NAME</b></dt>
</dl>
</td>
<td width="60%">
A pointer to an 
<a href="https://msdn.microsoft.com/ad91a302-f693-44e9-9655-ec4488ff78c4">OBJECTS_AND_NAME</a> structure that contains the name of the trustee and the names of the object types in an object-specific ACE.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUSTEE_IS_OBJECTS_AND_SID"></a><a id="trustee_is_objects_and_sid"></a><dl>
<dt><b>TRUSTEE_IS_OBJECTS_AND_SID</b></dt>
</dl>
</td>
<td width="60%">
A pointer to an 
<a href="https://msdn.microsoft.com/77ba8a3c-01e5-4a3e-835f-c7b9ef60035a">OBJECTS_AND_SID</a> structure that contains the SID of the trustee and the GUIDs of the object types in an object-specific ACE.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUSTEE_IS_SID"></a><a id="trustee_is_sid"></a><dl>
<dt><b>TRUSTEE_IS_SID</b></dt>
</dl>
</td>
<td width="60%">
 Pointer to the SID of the trustee.

</td>
</tr>
</table>
 


## -remarks



A trustee name can have any of the following formats:

<ul>
<li>A fully qualified name, such as "g:\remotedir\abc".</li>
<li>A domain account, such as "domain1\xyz".</li>
<li>One of the predefined group names, such as "EVERYONE" or "GUEST".</li>
<li>One of the following special names. <table>
<tr>
<th>Name</th>
<th>Meaning</th>
</tr>
<tr>
<td>CREATOR GROUP</td>
<td>The CREATOR_GROUP SID is a SID used in inheritable ACEs. When a new object is created, the system replaces this SID with the primary group SID of the user who created the object.</td>
</tr>
<tr>
<td>CREATOR OWNER</td>
<td>The CREATOR_OWNER SID is a SID used in inheritable ACEs. When a new object is created, the system replaces this SID with the SID of the user who created the object.</td>
</tr>
<tr>
<td>CURRENT_USER</td>
<td>The owner of the calling thread or process.</td>
</tr>
</table>
 

</li>
</ul>
A trustee SID can be any user or group SID. It can also be any of the <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">universal, well-known SIDs</a>. For more information, see 
<a href="https://msdn.microsoft.com/7cb07bcd-70f4-43dd-8382-320fcff151c7">Security Identifiers</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a>



<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a>



<a href="https://msdn.microsoft.com/186aa6aa-efc3-4f8a-acad-e257da3dac0b">GetExplicitEntriesFromAcl</a>



<a href="https://msdn.microsoft.com/00b00678-5c87-4aa9-8232-5f0f1cb48e24">MULTIPLE_TRUSTEE_OPERATION</a>



<a href="https://msdn.microsoft.com/ad91a302-f693-44e9-9655-ec4488ff78c4">OBJECTS_AND_NAME</a>



<a href="https://msdn.microsoft.com/77ba8a3c-01e5-4a3e-835f-c7b9ef60035a">OBJECTS_AND_SID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>



<a href="https://msdn.microsoft.com/05960fc1-1ad2-4c19-a65c-62259af5e18c">SetEntriesInAcl</a>



<a href="https://msdn.microsoft.com/991ac6cb-3fc9-4915-b5c9-ae73efb25d68">TRUSTEE_FORM</a>



<a href="https://msdn.microsoft.com/6519c79d-9cee-4565-a71e-0b81a27c1185">TRUSTEE_TYPE</a>
 

 

