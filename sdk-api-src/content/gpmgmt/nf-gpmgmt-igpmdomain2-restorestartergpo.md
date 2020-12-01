---
UID: NF:gpmgmt.IGPMDomain2.RestoreStarterGPO
title: IGPMDomain2::RestoreStarterGPO (gpmgmt.h)
description: Restores the Starter Group Policy object (GPO) from a GPMStarterGPOBackup object.
helpviewer_keywords: ["IGPMDomain2 interface [GPMC]","RestoreStarterGPO method","IGPMDomain2.RestoreStarterGPO","IGPMDomain2::RestoreStarterGPO","RestoreStarterGPO","RestoreStarterGPO method [GPMC]","RestoreStarterGPO method [GPMC]","IGPMDomain2 interface","gpmc.igpmdomain2_restorestartergpo","gpmgmt/IGPMDomain2::RestoreStarterGPO"]
old-location: gpmc\igpmdomain2_restorestartergpo.htm
tech.root: gpmc
ms.assetid: e91a3540-7f1b-4843-9b5e-4dcd837dc0f8
ms.date: 12/05/2018
ms.keywords: IGPMDomain2 interface [GPMC],RestoreStarterGPO method, IGPMDomain2.RestoreStarterGPO, IGPMDomain2::RestoreStarterGPO, RestoreStarterGPO, RestoreStarterGPO method [GPMC], RestoreStarterGPO method [GPMC],IGPMDomain2 interface, gpmc.igpmdomain2_restorestartergpo, gpmgmt/IGPMDomain2::RestoreStarterGPO
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
 - IGPMDomain2::RestoreStarterGPO
 - gpmgmt/IGPMDomain2::RestoreStarterGPO
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
 - IGPMDomain2.RestoreStarterGPO
---

## -description

Restores the Starter Group Policy object (GPO) from a 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackup">GPMStarterGPOBackup</a> object. You can restore a Starter GPO only to the domain in which the Starter GPO was originally created. This is because the operation restores the Starter GPO with its original Starter GPO ID and policy settings.

## -parameters

### -param pIGPMTmplBackup [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackup">GPMStarterGPOBackup</a> object to restore.

### -param pvarGPMProgress [in, optional]

Specifies a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of the restore operation. The caller must create this interface and then pass the interface pointer in this parameter to receive asynchronous notifications. This parameter must be <b>NULL</b> if the client should not receive asynchronous notifications. The method runs asynchronously if  this parameter is not <b>NULL</b>, and the method runs synchronously if <b>NULL</b>.

### -param pvarGPMCancel [out, optional]

Receives a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a> interface that the client can use to cancel the restore operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.

### -param ppIGPMResult [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a> interface that represents the result of the restore operation. That interface contains pointers to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">IGPMstarterGPO</a> interface and to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a> interface.

## -returns

<h3>C++</h3>
 Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs. 

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

## -remarks

A restore operation returns the contents of a specific GPO to the status it had when the backup was performed.

You must check the code that is returned by the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmresult-overallstatus">IGPMResult::OverallStatus</a> method as well as the one returned by this method to determine whether or not the operation succeeded. 
<b>OverallStatus</b> returns an overall status code for the operation. If no error occurred during the operation, it returns a success code. Otherwise, it returns a failure code.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain2">IGPMDomain2</a>