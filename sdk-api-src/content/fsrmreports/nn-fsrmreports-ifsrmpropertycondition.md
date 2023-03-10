---
UID: NN:fsrmreports.IFsrmPropertyCondition
title: IFsrmPropertyCondition (fsrmreports.h)
description: Defines a property condition that the file management job uses to determine if the file is expired.
helpviewer_keywords: ["IFsrmPropertyCondition","IFsrmPropertyCondition interface [File Server Resource Manager]","IFsrmPropertyCondition interface [File Server Resource Manager]","described","fs.ifsrmpropertycondition","fsrm.ifsrmpropertycondition","fsrm/IFsrmPropertyCondition"]
old-location: fsrm\ifsrmpropertycondition.htm
tech.root: fsrm
ms.assetid: 5c50b86b-f166-459e-92ce-63faa374c407
ms.date: 12/05/2018
ms.keywords: IFsrmPropertyCondition, IFsrmPropertyCondition interface [File Server Resource Manager], IFsrmPropertyCondition interface [File Server Resource Manager],described, fs.ifsrmpropertycondition, fsrm.ifsrmpropertycondition, fsrm/IFsrmPropertyCondition
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
 - IFsrmPropertyCondition
 - fsrmreports/IFsrmPropertyCondition
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
 - IFsrmPropertyCondition
---

# IFsrmPropertyCondition interface


## -description

Defines a property condition that the file management job uses to determine if the file is expired.

To create this interface, call the <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-createpropertycondition">IFsrmFileManagementJob::CreatePropertyCondition</a>   method.

The <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_propertyconditions">IFsrmFileManagementJob.PropertyConditions</a> property contains a collection of these interfaces.

## -inheritance

The <b>IFsrmPropertyCondition</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmPropertyCondition</b> also has these types of members:

## -remarks

The property condition specifies the classification property in the file to test. When the file management job runs, it gets the value of the classification property and uses the comparison operator to compare the value of the specified classification property (see the [Value](./nf-fsrmreports-ifsrmpropertycondition-get_value.md) property). If this condition  and all the other specified conditions for the job are met, FSRM can expire the file or call the custom action if it is defined.
