---
UID: NF:gpmgmt.IGPM.CreateSearchCriteria
title: IGPM::CreateSearchCriteria (gpmgmt.h)
description: Creates and returns a GPMSearchCriteria that represents the criteria to use for performing search operations when you use the Group Policy Management Console (GPMC) interfaces.
helpviewer_keywords: ["CreateSearchCriteria","CreateSearchCriteria method [GPMC]","CreateSearchCriteria method [GPMC]","GPM class","CreateSearchCriteria method [GPMC]","IGPM interface","GPM class [GPMC]","CreateSearchCriteria method","IGPM interface [GPMC]","CreateSearchCriteria method","IGPM.CreateSearchCriteria","IGPM::CreateSearchCriteria","_win32_igpm_createsearchcriteria","gpmc.igpm_createsearchcriteria","gpmgmt/IGPM::CreateSearchCriteria"]
old-location: gpmc\igpm_createsearchcriteria.htm
tech.root: gpmc
ms.assetid: 7bb99109-c0d6-47cb-9ea4-6c60c1607b79
ms.date: 12/05/2018
ms.keywords: CreateSearchCriteria, CreateSearchCriteria method [GPMC], CreateSearchCriteria method [GPMC],GPM class, CreateSearchCriteria method [GPMC],IGPM interface, GPM class [GPMC],CreateSearchCriteria method, IGPM interface [GPMC],CreateSearchCriteria method, IGPM.CreateSearchCriteria, IGPM::CreateSearchCriteria, _win32_igpm_createsearchcriteria, gpmc.igpm_createsearchcriteria, gpmgmt/IGPM::CreateSearchCriteria
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
 - IGPM::CreateSearchCriteria
 - gpmgmt/IGPM::CreateSearchCriteria
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
 - IGPM.CreateSearchCriteria
 - GPM.CreateSearchCriteria
---

# IGPM::CreateSearchCriteria


## -description

Creates and returns a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">GPMSearchCriteria</a> that represents the criteria to use for performing search operations when you use the Group Policy Management Console (GPMC) interfaces.

## -parameters

### -param ppIGPMSearchCriteria [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">IGPMSearchCriteria</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMSearchCriteria</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMSearchCriteria</b> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">IGPMSearchCriteria</a>