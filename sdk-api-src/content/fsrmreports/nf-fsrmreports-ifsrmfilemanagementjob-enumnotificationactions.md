---
UID: NF:fsrmreports.IFsrmFileManagementJob.EnumNotificationActions
title: IFsrmFileManagementJob::EnumNotificationActions (fsrmreports.h)
description: Enumerates the actions associated with a notification value.helpviewer_keywords: ["EnumNotificationActions","EnumNotificationActions method [File Server Resource Manager]","EnumNotificationActions method [File Server Resource Manager]","IFsrmFileManagementJob interface","IFsrmFileManagementJob interface [File Server Resource Manager]","EnumNotificationActions method","IFsrmFileManagementJob.EnumNotificationActions","IFsrmFileManagementJob::EnumNotificationActions","fs.ifsrmfilemanagementjob_enumnotificationactions","fsrm.ifsrmfilemanagementjob_enumnotificationactions","fsrmreports/IFsrmFileManagementJob::EnumNotificationActions"]
old-location: fsrm\ifsrmfilemanagementjob_enumnotificationactions.htm
tech.root: fsrm
ms.assetid: cfb58db2-39af-434e-95e2-abbd21f4487a
ms.date: 12/05/2018
ms.keywords: EnumNotificationActions, EnumNotificationActions method [File Server Resource Manager], EnumNotificationActions method [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],EnumNotificationActions method, IFsrmFileManagementJob.EnumNotificationActions, IFsrmFileManagementJob::EnumNotificationActions, fs.ifsrmfilemanagementjob_enumnotificationactions, fsrm.ifsrmfilemanagementjob_enumnotificationactions, fsrmreports/IFsrmFileManagementJob::EnumNotificationActions
f1_keywords:
- fsrmreports/IFsrmFileManagementJob.EnumNotificationActions
dev_langs:
- c++
req.header: fsrmreports.h
req.include-header: 
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- SrmSvc.dll
api_name:
- IFsrmFileManagementJob.EnumNotificationActions
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmFileManagementJob::EnumNotificationActions


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

Enumerates the actions associated with a notification value.


## -parameters




### -param days [in]

The notification value that contains the actions that you want to enumerate.


### -param actions [out]

An <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a> interface that contains a  collection of actions. The variant type of each item in the collection is <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant to get an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmaction">IFsrmAction</a> interface. You can use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmaction-get_actiontype">IFsrmAction::ActionType</a> property to determine the actual action interface to query.


## -returns



The method returns the following return values.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-createnotificationaction">IFsrmFileManagementJob::CreateNotificationAction</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>
 

 

