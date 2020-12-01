---
UID: NF:gpmgmt.IGPMAsyncProgress.Status
title: IGPMAsyncProgress::Status (gpmgmt.h)
description: The server calls this method to notify the client about the status of a Group Policy Management Console (GPMC) operation.
helpviewer_keywords: ["IGPMAsyncProgress interface [GPMC]","Status method","IGPMAsyncProgress.Status","IGPMAsyncProgress::Status","Status","Status method [GPMC]","Status method [GPMC]","IGPMAsyncProgress interface","_win32_igpmasyncprogress_status","gpmc.igpmasyncprogress_status","gpmgmt/IGPMAsyncProgress::Status"]
old-location: gpmc\igpmasyncprogress_status.htm
tech.root: gpmc
ms.assetid: db5d59a2-ab46-42f1-9637-6b342795c9f0
ms.date: 12/05/2018
ms.keywords: IGPMAsyncProgress interface [GPMC],Status method, IGPMAsyncProgress.Status, IGPMAsyncProgress::Status, Status, Status method [GPMC], Status method [GPMC],IGPMAsyncProgress interface, _win32_igpmasyncprogress_status, gpmc.igpmasyncprogress_status, gpmgmt/IGPMAsyncProgress::Status
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
 - IGPMAsyncProgress::Status
 - gpmgmt/IGPMAsyncProgress::Status
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
 - IGPMAsyncProgress.Status
---

# IGPMAsyncProgress::Status


## -description

The server calls this method to notify the client about the status of a Group Policy Management Console (GPMC) operation.

## -parameters

### -param lProgressNumerator [in]

Numerator of a fraction that represents the percent of the GPMC operation that is complete.

### -param lProgressDenominator [in]

Denominator of a fraction that represents the percent of the GPMC operation that is complete. The value of this parameter is proportional to the number of extensions in the Group Policy object (GPO), whether the GPO is a "live" GPO or a backed-up GPO. This value can be used to display the progress bar to the user.

In the GPMC user interface, the progress bar is divided into <i>lProgressDenominator</i> intervals. When <i>lProgressNumerator</i>==<i>lProgressDenominator</i> the operation is complete.

### -param hrStatus [in]

Status of the operation. If no error occurred, the value of the parameter is <b>S_OK</b>.

### -param pResult [in]

Result of the operation. 
This parameter is an interface pointer to the object that resulted from the GPMC operation. For example, it may be a pointer to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">GPMGPO</a> object or to  a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> object. This object is only returned when the operation is complete.

### -param ppIGPMStatusMsgCollection [in]

A pointer to the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a> interface that contains detailed status information about the operation. In cases where there are no errors, or if there are no detailed messages, Status passes in a null collection.

## -returns

This method has no return values.

## -remarks

This method must be implemented by the client.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress</a>