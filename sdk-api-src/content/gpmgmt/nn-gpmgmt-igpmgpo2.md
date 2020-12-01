---
UID: NN:gpmgmt.IGPMGPO2
title: IGPMGPO2 (gpmgmt.h)
description: The IGPMGPO2 interface supports methods that enable you to manage Group Policy objects (GPOs) and Starter Group Policy objects in the directory service.
helpviewer_keywords: ["IGPMGPO2","IGPMGPO2 interface [GPMC]","IGPMGPO2 interface [GPMC]","described","gpmc.igpmgpo2","gpmgmt/IGPMGPO2"]
old-location: gpmc\igpmgpo2.htm
tech.root: gpmc
ms.assetid: c5c21ca6-2722-4821-8760-03b6cf2befa7
ms.date: 12/05/2018
ms.keywords: IGPMGPO2, IGPMGPO2 interface [GPMC], IGPMGPO2 interface [GPMC],described, gpmc.igpmgpo2, gpmgmt/IGPMGPO2
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
 - IGPMGPO2
 - gpmgmt/IGPMGPO2
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
 - IGPMGPO2
---

# IGPMGPO2 interface


## -description

The 
<b>IGPMGPO2</b> interface supports methods that enable you to manage Group Policy objects (GPOs) and Starter Group Policy objects in the directory service.

Note that you cannot use this interface to manage local GPOs (LGPOs).

You can instantiate a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">GPMGPO2</a> object by creating a new one with a call to 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-creategpo">IGPMDomain::CreateGPO</a>, or  <b>IGPMDomain2::CreateStarterGPO</b> retrieving an existing one with a call to 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-getgpo">IGPMDomain::GetGPO</a>, calling <b>IGPMDomain2::GetStarterGPO</b> or by searching for one with a call to 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-searchgpos">IGPMDomain::SearchGPOs</a>. You can also create a GPO from an existing Starter GPO with a call to <b>IGPMDomain2::CreateGPOFromStarterGPO</b>. After creating the object, you can query the GPO and set properties related to the GPO.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>



<b>IGPMDomain2</b>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">IGPMGPOCollection</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>