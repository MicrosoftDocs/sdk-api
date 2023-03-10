---
UID: NF:gpmgmt.IGPMSOM.GetInheritedGPOLinks
title: IGPMSOM::GetInheritedGPOLinks (gpmgmt.h)
description: Returns a GPOLinksCollection object that contains the GPO links that are applied to the scope of management (SOM), including links inherited from parent containers (OUs and domains).
helpviewer_keywords: ["GPMSOM class [GPMC]","GetInheritedGPOLinks method","GetInheritedGPOLinks","GetInheritedGPOLinks method [GPMC]","GetInheritedGPOLinks method [GPMC]","GPMSOM class","GetInheritedGPOLinks method [GPMC]","IGPMSOM interface","IGPMSOM interface [GPMC]","GetInheritedGPOLinks method","IGPMSOM.GetInheritedGPOLinks","IGPMSOM::GetInheritedGPOLinks","_win32_igpmsom_getinheritedgpolinks","gpmc.igpmsom_getinheritedgpolinks","gpmgmt/IGPMSOM::GetInheritedGPOLinks"]
old-location: gpmc\igpmsom_getinheritedgpolinks.htm
tech.root: gpmc
ms.assetid: 545ab05a-b25e-40a7-b002-6935587764a5
ms.date: 12/05/2018
ms.keywords: GPMSOM class [GPMC],GetInheritedGPOLinks method, GetInheritedGPOLinks, GetInheritedGPOLinks method [GPMC], GetInheritedGPOLinks method [GPMC],GPMSOM class, GetInheritedGPOLinks method [GPMC],IGPMSOM interface, IGPMSOM interface [GPMC],GetInheritedGPOLinks method, IGPMSOM.GetInheritedGPOLinks, IGPMSOM::GetInheritedGPOLinks, _win32_igpmsom_getinheritedgpolinks, gpmc.igpmsom_getinheritedgpolinks, gpmgmt/IGPMSOM::GetInheritedGPOLinks
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
 - IGPMSOM::GetInheritedGPOLinks
 - gpmgmt/IGPMSOM::GetInheritedGPOLinks
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
 - IGPMSOM.GetInheritedGPOLinks
 - GPMSOM.GetInheritedGPOLinks
---

# IGPMSOM::GetInheritedGPOLinks


## -description

Returns a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpolinkscollection">GPOLinksCollection</a> object that contains the GPO links that are applied to the scope of management (SOM), including links inherited from parent containers (OUs and domains). The collection does not include GPO links from site SOMs or disabled links. The collection is sorted in  order of precedence, with the first (earliest) link having the highest priority and last (latest) link having the lowest priority. Note that  the GPOs are applied in  reverse order of their precedence. The last GPO in the list is applied first and the first GPO in the list is applied last.

## -parameters

### -param ppGPOLinks [out]

Address of a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpolinkscollection">IGPMGPOLinksCollection</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpolinkscollection">GPOLinksCollection</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpolinkscollection">GPOLinksCollection</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpolink">IGPMGPOLink</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpolinkscollection">IGPMGPOLinksCollection</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsom">IGPMSOM</a>