---
UID: NF:gpmgmt.IGPMSitesContainer.GetSite
title: IGPMSitesContainer::GetSite (gpmgmt.h)
author: windows-sdk-content
description: Returns the scope of management (SOM) object that corresponds to the site.
old-location: gpmc\igpmsitescontainer_getsite.htm
tech.root: gpmc
ms.assetid: f8b459d0-d0f5-48b1-8870-487a1645ae7a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMSitesContainer class [GPMC],GetSite method, GetSite, GetSite method [GPMC], GetSite method [GPMC],GPMSitesContainer class, GetSite method [GPMC],IGPMSitesContainer interface, IGPMSitesContainer interface [GPMC],GetSite method, IGPMSitesContainer.GetSite, IGPMSitesContainer::GetSite, _win32_igpmsitescontainer_getsite, gpmc.igpmsitescontainer_getsite, gpmgmt/IGPMSitesContainer::GetSite
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
 - IGPMSitesContainer.GetSite
 - GPMSitesContainer.GetSite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMSitesContainer::GetSite


## -description


Returns the scope of management (SOM) object that corresponds to the site.


## -parameters




### -param bstrSiteName [in]

Required. The site of interest; for example, Default-first-site-name. Use null-terminated string.


### -param ppSOM [out]

Address of a pointer to the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsom">IGPMSOM</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMSOM</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMSOM</b> object.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsom">IGPMSOM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsitescontainer">IGPMSitesContainer</a>
 

 

