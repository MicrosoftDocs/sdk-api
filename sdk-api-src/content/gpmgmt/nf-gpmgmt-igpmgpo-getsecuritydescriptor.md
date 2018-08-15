---
UID: NF:gpmgmt.IGPMGPO.GetSecurityDescriptor
title: IGPMGPO::GetSecurityDescriptor
author: windows-sdk-content
description: Retrieves a pointer to an IDispatch interface from which the security descriptor for the Group Policy object (GPO) can be retrieved. For script programmers, this method returns a reference to an IADsSecurityDescriptor object.
old-location: gpmc\igpmgpo_getsecuritydescriptor.htm
old-project: GPMC
ms.assetid: 4035119b-2688-4326-8d08-825d53c3d8e2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: DACL_SECURITY_INFORMATION, GPMGPO class [GPMC],GetSecurityDescriptor method, GROUP_SECURITY_INFORMATION, GetSecurityDescriptor, GetSecurityDescriptor method [GPMC], GetSecurityDescriptor method [GPMC],GPMGPO class, GetSecurityDescriptor method [GPMC],IGPMGPO interface, IGPMGPO interface [GPMC],GetSecurityDescriptor method, IGPMGPO.GetSecurityDescriptor, IGPMGPO::GetSecurityDescriptor, OWNER_SECURITY_INFORMATION, SACL_SECURITY_INFORMATION, _win32_igpmgpo_getsecuritydescriptor, gpmc.igpmgpo_getsecuritydescriptor, gpmgmt/IGPMGPO::GetSecurityDescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: GPMStarterGPOType
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
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMGPO::GetSecurityDescriptor


## -description


Retrieves a pointer to an <b>IDispatch</b> interface from which the security descriptor for the Group Policy object (GPO) can be retrieved. For script programmers, this method returns a reference to an 
<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a> object.


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

Address of a pointer to an <b>IDispatch</b> interface. You can call the <a href="_com_iunknown_queryinterface">IUnknown::QueryInterface</a> method to obtain a pointer to the <a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a> interface on the security descriptor of the GPO.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to an 
<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a> object.

<h3>VB</h3>
Returns a reference to an 
<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a> object.




## -remarks



For more information about security descriptors, ACLs, and the security model for controlling access to Windows-based objects, see <a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>.




## -see-also




<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>
 

 

