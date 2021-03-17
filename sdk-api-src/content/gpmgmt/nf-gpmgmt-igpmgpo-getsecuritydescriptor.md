---
UID: NF:gpmgmt.IGPMGPO.GetSecurityDescriptor
title: IGPMGPO::GetSecurityDescriptor (gpmgmt.h)
description: Retrieves a pointer to an IDispatch interface from which the security descriptor for the Group Policy object (GPO) can be retrieved. For script programmers, this method returns a reference to an IADsSecurityDescriptor object.
helpviewer_keywords: ["DACL_SECURITY_INFORMATION","GPMGPO class [GPMC]","GetSecurityDescriptor method","GROUP_SECURITY_INFORMATION","GetSecurityDescriptor","GetSecurityDescriptor method [GPMC]","GetSecurityDescriptor method [GPMC]","GPMGPO class","GetSecurityDescriptor method [GPMC]","IGPMGPO interface","IGPMGPO interface [GPMC]","GetSecurityDescriptor method","IGPMGPO.GetSecurityDescriptor","IGPMGPO::GetSecurityDescriptor","OWNER_SECURITY_INFORMATION","SACL_SECURITY_INFORMATION","_win32_igpmgpo_getsecuritydescriptor","gpmc.igpmgpo_getsecuritydescriptor","gpmgmt/IGPMGPO::GetSecurityDescriptor"]
old-location: gpmc\igpmgpo_getsecuritydescriptor.htm
tech.root: gpmc
ms.assetid: 4035119b-2688-4326-8d08-825d53c3d8e2
ms.date: 12/05/2018
ms.keywords: DACL_SECURITY_INFORMATION, GPMGPO class [GPMC],GetSecurityDescriptor method, GROUP_SECURITY_INFORMATION, GetSecurityDescriptor, GetSecurityDescriptor method [GPMC], GetSecurityDescriptor method [GPMC],GPMGPO class, GetSecurityDescriptor method [GPMC],IGPMGPO interface, IGPMGPO interface [GPMC],GetSecurityDescriptor method, IGPMGPO.GetSecurityDescriptor, IGPMGPO::GetSecurityDescriptor, OWNER_SECURITY_INFORMATION, SACL_SECURITY_INFORMATION, _win32_igpmgpo_getsecuritydescriptor, gpmc.igpmgpo_getsecuritydescriptor, gpmgmt/IGPMGPO::GetSecurityDescriptor
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMGPO::GetSecurityDescriptor
 - gpmgmt/IGPMGPO::GetSecurityDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMGPO.GetSecurityDescriptor
 - GPMGPO.GetSecurityDescriptor
---

# IGPMGPO::GetSecurityDescriptor


## -description

Retrieves a pointer to an <b>IDispatch</b> interface from which the security descriptor for the Group Policy object (GPO) can be retrieved. For script programmers, this method returns a reference to an 
<a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a> object.

## -parameters

### -param lFlags [in]

Specifies a set of bit flags. Use this parameter to specify the parts of the security descriptor to retrieve. The following values are valid.



#### OWNER_SECURITY_INFORMATION (1)

Owner identifier of the object.



#### GROUP_SECURITY_INFORMATION (2)

Primary group identifier.



#### DACL_SECURITY_INFORMATION (4)

Discretionary access control list (DACL) of the object.



#### SACL_SECURITY_INFORMATION (8)

System access control list (ACL) of the object.

### -param ppSD [out]

Address of a pointer to an <b>IDispatch</b> interface. You can call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to obtain a pointer to the <a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a> interface on the security descriptor of the GPO.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to an 
<a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a> object.

<h3>VB</h3>
Returns a reference to an 
<a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a> object.

## -remarks

For more information about security descriptors, ACLs, and the security model for controlling access to Windows-based objects, see <a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>