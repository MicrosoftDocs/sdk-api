---
UID: NF:gpmgmt.IGPMDomain.GetSOM
title: IGPMDomain::GetSOM (gpmgmt.h)
author: windows-sdk-content
description: Retrieves the IGPMSOM interface that represents the domain or the organizational unit (OU) at the specified path.
old-location: gpmc\igpmdomain_getsom.htm
tech.root: gpmc
ms.assetid: cbacd900-26ea-4554-97d8-8f33d2f5dd2b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMDomain class [GPMC],GetSOM method, GetSOM, GetSOM method [GPMC], GetSOM method [GPMC],GPMDomain class, GetSOM method [GPMC],IGPMDomain interface, IGPMDomain interface [GPMC],GetSOM method, IGPMDomain.GetSOM, IGPMDomain::GetSOM, _win32_igpmdomain_getsom, gpmc.igpmdomain_getsom, gpmgmt/IGPMDomain::GetSOM
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMDomain.GetSOM
 - GPMDomain.GetSOM
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMDomain::GetSOM


## -description


Retrieves the <a href="https://msdn.microsoft.com/e3252dba-403d-486d-b666-9bb04ec0aa90">IGPMSOM</a> interface that represents the domain or the organizational unit  (OU) at the specified path.


## -parameters




### -param bstrPath [in]

Path of the scope of management (SOM) object.  The path must be a fully qualified distinguished name. Use the following syntax for the path: (ou=<i>MyOU</i>,dc=<i>domain_name</i>,dc=<i>com</i>).

<b>C++:  </b>If <b>NULL</b> is specified, the method returns a pointer to the 
<b>IGPMSOM</b> interface for the domain.

<b>Scripting:  </b>If an empty string ("") is specified, the method returns a pointer to the 
<b>IGPMSOM</b> interface for the domain.


### -param ppSOM [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/e3252dba-403d-486d-b666-9bb04ec0aa90">IGPMSOM</a> interface at the specified path.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMSOM</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMSOM</b> object.




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMDomain</a>



<a href="https://msdn.microsoft.com/e3252dba-403d-486d-b666-9bb04ec0aa90">IGPMSOM</a>
 

 

