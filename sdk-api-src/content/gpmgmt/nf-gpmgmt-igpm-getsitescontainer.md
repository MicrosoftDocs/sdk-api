---
UID: NF:gpmgmt.IGPM.GetSitesContainer
title: IGPM::GetSitesContainer
author: windows-sdk-content
description: Creates and returns a GPMSitesContainer object from which sites can be opened and queried.
old-location: gpmc\igpm_getsitescontainer.htm
old-project: GPMC
ms.assetid: 0a1b8975-cd73-49e6-83b9-f6af296276cb
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: GPM object [GPMC],GetSitesContainer method, GetSitesContainer, GetSitesContainer method [GPMC], GetSitesContainer method [GPMC],GPM object, GetSitesContainer method [GPMC],IGPM interface, IGPM interface [GPMC],GetSitesContainer method, IGPM.GetSitesContainer, IGPM::GetSitesContainer, _win32_igpm_getsitescontainer, gpmc.igpm_getsitescontainer, gpmgmt/IGPM::GetSitesContainer
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPM.GetSitesContainer
-	GPM.GetSitesContainer
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
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
 

 

