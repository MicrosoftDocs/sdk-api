---
UID: NF:fsrmreports.IFsrmFileManagementJob.EnumNotificationActions
title: IFsrmFileManagementJob::EnumNotificationActions (fsrmreports.h)
author: windows-sdk-content
description: Enumerates the actions associated with a notification value.
old-location: fsrm\ifsrmfilemanagementjob_enumnotificationactions.htm
tech.root: fsrm
ms.assetid: cfb58db2-39af-434e-95e2-abbd21f4487a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumNotificationActions, EnumNotificationActions method [File Server Resource Manager], EnumNotificationActions method [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],EnumNotificationActions method, IFsrmFileManagementJob.EnumNotificationActions, IFsrmFileManagementJob::EnumNotificationActions, fs.ifsrmfilemanagementjob_enumnotificationactions, fsrm.ifsrmfilemanagementjob_enumnotificationactions, fsrmreports/IFsrmFileManagementJob::EnumNotificationActions
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmFileManagementJob::EnumNotificationActions


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

Enumerates the actions associated with a notification value.


## -parameters




### -param days [in]

The notification value that contains the actions that you want to enumerate.


### -param actions [out]

An <a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a> interface that contains a  collection of actions. The variant type of each item in the collection is <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant to get an <a href="https://msdn.microsoft.com/81bfae1d-7d09-4ddc-9669-1da40dc72fd4">IFsrmAction</a> interface. You can use the <a href="https://msdn.microsoft.com/7ce0bafb-8076-4a0d-bd59-9e2d436f74c1">IFsrmAction::ActionType</a> property to determine the actual action interface to query.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/d0cb2ac1-842c-4ebb-adac-8298a0e0beed">IFsrmFileManagementJob::CreateNotificationAction</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

