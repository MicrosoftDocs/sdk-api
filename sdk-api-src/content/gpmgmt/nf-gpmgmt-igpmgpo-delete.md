---
UID: NF:gpmgmt.IGPMGPO.Delete
title: IGPMGPO::Delete (gpmgmt.h)
description: Deletes a Group Policy object (GPO) from the directory service and from the system volume folder (SYSVOL).
helpviewer_keywords: ["Delete","Delete method [GPMC]","Delete method [GPMC]","GPMGPO class","Delete method [GPMC]","IGPMGPO interface","GPMGPO class [GPMC]","Delete method","IGPMGPO interface [GPMC]","Delete method","IGPMGPO.Delete","IGPMGPO::Delete","_win32_igpmgpo_delete","gpmc.igpmgpo_delete","gpmgmt/IGPMGPO::Delete"]
old-location: gpmc\igpmgpo_delete.htm
tech.root: gpmc
ms.assetid: 63a29bf5-bac5-43af-87ec-01c3c2a5b3af
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [GPMC], Delete method [GPMC],GPMGPO class, Delete method [GPMC],IGPMGPO interface, GPMGPO class [GPMC],Delete method, IGPMGPO interface [GPMC],Delete method, IGPMGPO.Delete, IGPMGPO::Delete, _win32_igpmgpo_delete, gpmc.igpmgpo_delete, gpmgmt/IGPMGPO::Delete
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
 - IGPMGPO::Delete
 - gpmgmt/IGPMGPO::Delete
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
 - IGPMGPO.Delete
 - GPMGPO.Delete
---

# IGPMGPO::Delete


## -description

Deletes a Group Policy object (GPO) from the directory service and from the system volume folder (SYSVOL).



## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -remarks

This method does not delete GPO links. To delete GPO links, call the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpolink-delete">IGPMGPOLink::Delete</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>
