---
UID: NN:iads.IADsAccessControlEntry
title: IADsAccessControlEntry
author: windows-sdk-content
description: The IADsAccessControlEntry interface is a dual interface that enables directory clients to access and manipulate individual access-control entries (ACEs) of the owning object.
old-location: adsi\iadsaccesscontrolentry.htm
old-project: ADSI
ms.assetid: 6d2cd45b-0dc6-4bb3-9c41-014bec71f258
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: AccessControlEntry, IADsAccessControlEntry, IADsAccessControlEntry interface [ADSI], IADsAccessControlEntry interface [ADSI],described, _ds_iadsaccesscontrolentry, adsi.iadsaccesscontrolentry, iads/IADsAccessControlEntry
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: iads.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsAccessControlEntry
 - AccessControlEntry
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsAccessControlEntry interface


## -description


The <b>IADsAccessControlEntry</b> interface is a dual 
    interface that enables directory clients to access and manipulate individual access-control entries (ACEs) of the 
    owning object. An ACE stipulates who can access the object and what type of access  granted and specifies whether 
    the access control settings can be propagated from the object to any of its children. An ACE exposes a set of 
    properties through this interface to provide such services.

An object can have a number of ACEs, one for each client or a group of clients. ACEs are maintained in an 
    access-control list (ACL) which implements the 
    <a href="https://msdn.microsoft.com/de92d9cc-bc9d-4dc5-aa79-01f4d3050c35">IADsAccessControlList</a> interface. That is, a client 
    must use an ACL to access an ACE. To access the ACL, retrieve the  security descriptor of the object that 
    implements the  <a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a> interface. 
    The following procedures describe how to manage access controls over an ADSI object.

Some of the <b>IADsAccessControlEntry</b> property 
    values, such as <a href="https://msdn.microsoft.com/dce11723-0e30-4baa-8666-0a32f0968ebb">AccessMask</a> and 
    <b>AceFlags</b>, will be different 
    for different object types. For example, an Active Directory object will use the 
    <b>ADS_RIGHT_GENERIC_READ</b> member of the 
    <a href="https://msdn.microsoft.com/ade64dd8-e08c-4f68-b3bf-ccc252272a99">ADS_RIGHTS_ENUM</a> enumeration for the 
    <b>IADsAccessControlEntry.AccessMask</b> 
    property, but the equivalent access right for a file object is <b>FILE_GENERIC_READ</b>. It is 
    not safe to assume that all property values will be the same for Active Directory objects and non-Active Directory 
    objects. For more information, see 
    <a href="https://msdn.microsoft.com/7233a82f-fc38-4718-b674-4e6a00666184">Security Descriptors on Files and Registry Keys</a>.
<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To managing access controls over an ADSI object</b>
<ol>
<li>Retrieve the security descriptor for the object that implements the 
     <a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a> interface.</li>
<li>Retrieve the ACL from the security descriptor.</li>
<li>Work with the ACE, or ACEs, of the object in the 
     ACL.</li>
</ol><p class="proch"><img alt="" src="../common/wedge.gif"/><b>To set a new or modified ACE as persistent</b>
<ol>
<li>Add the ACE to the ACL.</li>
<li>Assign the ACL to the security descriptor.</li>
<li>Commit the security descriptor to the directory store.</li>
</ol>

## -see-also




<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/de92d9cc-bc9d-4dc5-aa79-01f4d3050c35">IAccessControlList</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

