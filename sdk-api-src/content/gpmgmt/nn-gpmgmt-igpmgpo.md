---
UID: NN:gpmgmt.IGPMGPO
title: IGPMGPO (gpmgmt.h)
description: The IGPMGPO interface supports methods that enable you to manage Group Policy Objects (GPOs) in the directory service.
helpviewer_keywords: ["GPMGPO","IGPMGPO","IGPMGPO interface [GPMC]","IGPMGPO interface [GPMC]","described","_win32_igpmgpo","gpmc.igpmgpo","gpmgmt/ IGPMGPO"]
old-location: gpmc\igpmgpo.htm
tech.root: gpmc
ms.assetid: 2857c8b7-019d-4ec2-9a00-574fc8541cae
ms.date: 12/05/2018
ms.keywords: GPMGPO, IGPMGPO, IGPMGPO interface [GPMC], IGPMGPO interface [GPMC],described, _win32_igpmgpo, gpmc.igpmgpo, gpmgmt/ IGPMGPO
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
 - IGPMGPO
 - gpmgmt/IGPMGPO
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
 - IGPMGPO
 - GPMGPO
---

# IGPMGPO interface


## -description

The 
<b>IGPMGPO</b> interface supports methods that enable you to manage Group Policy Objects (GPOs) in the directory service.

Note that you cannot use this interface to manage local GPOs (LGPOs).

You can instantiate a <b>GPMGPO</b> object by creating a new one with a call to 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-creategpo">IGPMDomain::CreateGPO</a>, retrieving an existing one with a call to 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-getgpo">IGPMDomain::GetGPO</a>, or by searching for one with a call to 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-searchgpos">IGPMDomain::SearchGPOs</a>. After creating the object, you can query the GPO and set properties related to the GPO.

## -inheritance

The <b> IGPMGPO</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b> IGPMGPO</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">IGPMGPOCollection</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>
