---
UID: NF:fsrmquota.IFsrmQuotaBase.EnumThresholdActions
title: IFsrmQuotaBase::EnumThresholdActions method
author: windows-driver-content
description: Enumerates all the actions for the specified threshold.
old-location: fsrm\ifsrmquotabase_enumthresholdactions.htm
old-project: Fsrm
ms.assetid: ce4f85a9-f2e0-42df-adb4-7c21256d5305
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: EnumThresholdActions method [File Server Resource Manager], EnumThresholdActions method [File Server Resource Manager], IFsrmQuotaBase interface, EnumThresholdActions,IFsrmQuotaBase.EnumThresholdActions, IFsrmQuotaBase, IFsrmQuotaBase interface [File Server Resource Manager], EnumThresholdActions method, IFsrmQuotaBase::EnumThresholdActions, fs.ifsrmquotabase_enumthresholdactions, fsrm.ifsrmquotabase_enumthresholdactions, fsrmquota/IFsrmQuotaBase::EnumThresholdActions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: fsrmquota.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmQuotaBase.EnumThresholdActions
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmQuotaBase::EnumThresholdActions method


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Enumerates all the actions for the specified threshold.


## -parameters




### -param threshold [in]

The threshold that contains the actions that you want to enumerate.


### -param actions [out]

An <a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a> interface that contains a 
      collection of actions. The variant type of each item in the collection is <b>VT_DISPATCH</b>. 
      Query the <b>pdispVal</b> member of the variant to get an 
      <a href="https://msdn.microsoft.com/81bfae1d-7d09-4ddc-9669-1da40dc72fd4">IFsrmAction</a> interface. You can use the 
      <a href="https://msdn.microsoft.com/7ce0bafb-8076-4a0d-bd59-9e2d436f74c1">IFsrmAction::ActionType</a> property to determine 
      the actual action interface to query.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/7f4d5a73-a836-4ea1-bc53-d51433eeb02e">IFsrmQuotaBase</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

