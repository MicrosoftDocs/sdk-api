---
UID: NN:iads.IADsAccessControlEntry
title: IADsAccessControlEntry (iads.h)
description: The IADsAccessControlEntry interface is a dual interface that enables directory clients to access and manipulate individual access-control entries (ACEs) of the owning object.
helpviewer_keywords: ["AccessControlEntry","IADsAccessControlEntry","IADsAccessControlEntry interface [ADSI]","IADsAccessControlEntry interface [ADSI]","described","_ds_iadsaccesscontrolentry","adsi.iadsaccesscontrolentry","iads/IADsAccessControlEntry"]
old-location: adsi\iadsaccesscontrolentry.htm
tech.root: adsi
ms.assetid: 6d2cd45b-0dc6-4bb3-9c41-014bec71f258
ms.date: 12/05/2018
ms.keywords: AccessControlEntry, IADsAccessControlEntry, IADsAccessControlEntry interface [ADSI], IADsAccessControlEntry interface [ADSI],described, _ds_iadsaccesscontrolentry, adsi.iadsaccesscontrolentry, iads/IADsAccessControlEntry
req.header: iads.h
req.include-header: 
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
req.lib: 
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsAccessControlEntry
 - iads/IADsAccessControlEntry
dev_langs:
 - c++
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
    <a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist">IADsAccessControlList</a> interface. That is, a client 
    must use an ACL to access an ACE. To access the ACL, retrieve the  security descriptor of the object that 
    implements the  <a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a> interface. 
    The following procedures describe how to manage access controls over an ADSI object.

Some of the <b>IADsAccessControlEntry</b> property 
    values, such as <a href="/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods">AccessMask</a> and 
    <b>AceFlags</b>, will be different 
    for different object types. For example, an Active Directory object will use the 
    <b>ADS_RIGHT_GENERIC_READ</b> member of the 
    <a href="/windows/win32/api/iads/ne-iads-ads_rights_enum">ADS_RIGHTS_ENUM</a> enumeration for the 
    <b>IADsAccessControlEntry.AccessMask</b> 
    property, but the equivalent access right for a file object is <b>FILE_GENERIC_READ</b>. It is 
    not safe to assume that all property values will be the same for Active Directory objects and non-Active Directory 
    objects. For more information, see 
    <a href="/windows/desktop/ADSI/security-descriptors-on-files-and-registry-keys">Security Descriptors on Files and Registry Keys</a>.
<p class="proch"><b>To managing access controls over an ADSI object</b>
<ol>
<li>Retrieve the security descriptor for the object that implements the 
     <a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a> interface.</li>
<li>Retrieve the ACL from the security descriptor.</li>
<li>Work with the ACE, or ACEs, of the object in the 
     ACL.</li>
</ol><p class="proch"><b>To set a new or modified ACE as persistent</b>
<ol>
<li>Add the ACE to the ACL.</li>
<li>Assign the ACL to the security descriptor.</li>
<li>Commit the security descriptor to the directory store.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist">IAccessControlList</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>