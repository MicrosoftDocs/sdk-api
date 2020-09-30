---
UID: NF:gpmgmt.IGPMDomain2.LoadStarterGPO
title: IGPMDomain2::LoadStarterGPO (gpmgmt.h)
description: Opens a Starter Group Policy object (GPO) cabinet (CAB) file and imports it into the domain.
helpviewer_keywords: ["IGPMDomain2 interface [GPMC]","LoadStarterGPO method","IGPMDomain2.LoadStarterGPO","IGPMDomain2::LoadStarterGPO","LoadStarterGPO","LoadStarterGPO method [GPMC]","LoadStarterGPO method [GPMC]","IGPMDomain2 interface","gpmc.igpmdomain2_loadstartergpo","gpmgmt/IGPMDomain2::LoadStarterGPO"]
old-location: gpmc\igpmdomain2_loadstartergpo.htm
tech.root: gpmc
ms.assetid: 3375ecaf-6128-4bc0-9cfc-e9b00bf4b70a
ms.date: 12/05/2018
ms.keywords: IGPMDomain2 interface [GPMC],LoadStarterGPO method, IGPMDomain2.LoadStarterGPO, IGPMDomain2::LoadStarterGPO, LoadStarterGPO, LoadStarterGPO method [GPMC], LoadStarterGPO method [GPMC],IGPMDomain2 interface, gpmc.igpmdomain2_loadstartergpo, gpmgmt/IGPMDomain2::LoadStarterGPO
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
 - IGPMDomain2::LoadStarterGPO
 - gpmgmt/IGPMDomain2::LoadStarterGPO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gpmgmt.dll
api_name:
 - IGPMDomain2.LoadStarterGPO
---

# IGPMDomain2::LoadStarterGPO


## -description

Opens a Starter Group Policy object (GPO) cabinet (CAB) file and imports it into the domain.

## -parameters

### -param bstrLoadFile [in]

Required. Name of the CAB file to load. Use a null-terminated string.

### -param bOverwrite [in]

Determines whether to overwrite any existing versions of the Starter GPO.  Loading a Starter GPO from a CAB retains the ID of the original Starter GPO used to create the CAB, therefore it is possible to have a version of the Starter GPO already existing in the domain when the <b>LoadStarterGPO</b> method is called.



#### VARIANT_FALSE

Do not overwrite an existing Starter GPO.



#### VARIANT_TRUE

Overwrite an existing Starter GPO.

### -param pvarGPMProgress [in, optional]

Specifies a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of the copy operation. This parameter must be <b>NULL</b> if the client does not receive asynchronous notifications.

### -param pvarGPMCancel [out, optional]

Receives a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a> interface that the client can use to cancel the copy operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.

### -param ppIGPMResult [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a> interface that represents the result of the load operation. That interface contains pointers to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMStarterGPO</a> interface and to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain2">IGPMDomain2</a>