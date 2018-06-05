---
UID: NF:fsrmpipeline.IFsrmPropertyBag.AddMessage
title: IFsrmPropertyBag::AddMessage
author: windows-sdk-content
description: Adds an error message to the bag.
old-location: fsrm\ifsrmpropertybag_addmessage.htm
old-project: Fsrm
ms.assetid: 2d9166fd-5211-4114-843f-2c6563941715
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: AddMessage, AddMessage method [File Server Resource Manager], AddMessage method [File Server Resource Manager],IFsrmPropertyBag interface, IFsrmPropertyBag interface [File Server Resource Manager],AddMessage method, IFsrmPropertyBag.AddMessage, IFsrmPropertyBag::AddMessage, fs.ifsrmpropertybag_addmessage, fsrm.ifsrmpropertybag_addmessage, fsrmpipeline/IFsrmPropertyBag::AddMessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmpipeline.h
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmPropertyBag.AddMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmPropertyBag::AddMessage


## -description


Adds an error message to the bag.


## -parameters




### -param message [in]

The error message to add to the bag. The message is limited to 4096 characters (the message is truncated if longer than 4096 characters).


## -returns



The method returns the following return values.




## -remarks



You can add only one message to the bag. The message is written to the error log, if enabled.

If any of the following implementations returns an error code, FSRM automatically adds a message (which does not count against the one-message limit) that includes the error code and associated message string:

<ul>
<li>
<a href="https://msdn.microsoft.com/ab42430c-1e30-4576-b6f8-c0488b6230dd">IFsrmClassifierModuleImplementation::DoesPropertyValueApply</a>
</li>
<li>
<a href="https://msdn.microsoft.com/70277473-de96-40e1-980b-4eec6e7b035d">IFsrmClassifierModuleImplementation::GetPropertyValueToApply</a>
</li>
<li>
<a href="https://msdn.microsoft.com/05de6dfe-0f90-4866-bedc-72b8fea9dfac">IFsrmStorageModuleImplementation::LoadProperties</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4d31db26-9d03-46f3-a902-401f9e0d9767">IFsrmStorageModuleImplementation::SaveProperties</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/237f024d-2b1d-45d5-a63d-c530426278e6">IFsrmPropertyBag</a>



<a href="https://msdn.microsoft.com/3aa6bc28-03bb-40ea-8c56-94133c8eeb54">IFsrmPropertyBag::Messages</a>
 

 

