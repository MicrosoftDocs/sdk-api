---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IGPM::GetSitesContainer


## -description


Creates and returns a 
<a href="https://msdn.microsoft.com/e3fdfd44-9e90-4206-b7e9-97d4ed6eb8af">GPMSitesContainer</a> object from which sites can be opened and queried.


## -parameters




### -param bstrForest [in]

Required. Full DNS name of the forest in which to access sites; this is the name of the forest root domain. Use null-terminated string.


### -param bstrDomain [in]

Name of the domain in which to access sites. If specified, this must be a full Domain Name Server (DNS) name, such as example.microsoft.com. If a domain is specified in the <i>bstrDomain</i> parameter, the Group Policy Management Console (GPMC) accesses sites through that domain. If no domain is  specified, the GPMC accesses the sites through the forest that is specified in the <i>bstrForest</i> parameter. Use a null-terminated string.


### -param bstrDomainController [in]

If specified, the name of the domain controller to use with the domain specified in the <i>bstrDomain</i> parameter. The name can be a DNS name or a NetBIOS name. Otherwise, the method uses the primary domain controller (PDC). Use a null-terminated string.


### -param lDCFlags [in]

Flags to use to locate the domain controller for the domain. Currently, the only supported value is GPM_USE_ANYDC. If this parameter is set to zero, and <i>bstrDomainController</i> is specified, the method uses the specified domain controller. Otherwise, the method uses the PDC.


### -param ppIGPMSitesContainer [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/e3fdfd44-9e90-4206-b7e9-97d4ed6eb8af">IGPMSitesContainer</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/e3fdfd44-9e90-4206-b7e9-97d4ed6eb8af">GPMSitesContainer</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/e3fdfd44-9e90-4206-b7e9-97d4ed6eb8af">GPMSitesContainer</a> object.




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/e3fdfd44-9e90-4206-b7e9-97d4ed6eb8af">IGPMSitesContainer</a>
 

 

