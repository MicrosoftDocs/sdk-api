---
UID: NN:fsrmreports.IFsrmFileManagementJobManager
title: IFsrmFileManagementJobManager (fsrmreports.h)
description: Used to manage file management jobs.
helpviewer_keywords: ["IFsrmFileManagementJobManager","IFsrmFileManagementJobManager interface [File Server Resource Manager]","IFsrmFileManagementJobManager interface [File Server Resource Manager]","described","fs.ifsrmfilemanagementjobmanager","fsrm.ifsrmfilemanagementjobmanager","fsrm/IFsrmFileManagementJobManager"]
old-location: fsrm\ifsrmfilemanagementjobmanager.htm
tech.root: fsrm
ms.assetid: 2df0e8d0-1da7-422e-8d02-ad5d030fdd8d
ms.date: 12/05/2018
ms.keywords: IFsrmFileManagementJobManager, IFsrmFileManagementJobManager interface [File Server Resource Manager], IFsrmFileManagementJobManager interface [File Server Resource Manager],described, fs.ifsrmfilemanagementjobmanager, fsrm.ifsrmfilemanagementjobmanager, fsrm/IFsrmFileManagementJobManager
req.header: fsrmreports.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmFileManagementJobManager
 - fsrmreports/IFsrmFileManagementJobManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmFileManagementJobManager
---

# IFsrmFileManagementJobManager interface


## -description

Used to manage file management jobs.

To get this interface, call the 
    <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmFileManagementJobManager</b> as the class identifier and 
    <code>__uuidof(IFsrmFileManagementJobManager)</code> as the interface 
    identifier.

## -inheritance

The <b>IFsrmFileManagementJobManager</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmFileManagementJobManager</b> also has these types of members:

## -remarks

To create this object from a script, use the "Fsrm.FsrmFileManagementJobManager" program identifier.

A file management job consumes the classification properties associated with a file. The job performs actions 
    based whether the property values set by classification meet the specified file management property conditions. 
    The primary action is to expire the file (move the file to an expired files folder) and send notification that the 
    file was expired; however, you can also perform custom actions.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/fsrm/fsrmfilemanagementjobmanager">FsrmFileManagementJobManager</a>
