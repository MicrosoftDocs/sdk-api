---
UID: NF:fsrmquota.IFsrmQuotaObject.ApplyTemplate
title: IFsrmQuotaObject::ApplyTemplate
author: windows-sdk-content
description: Applies the property values of the specified quota template to this quota object.
old-location: fsrm\ifsrmquotaobject_applytemplate.htm
old-project: fsrm
ms.assetid: f4e65d53-7841-4f84-9c14-bad43089a87f
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: ApplyTemplate, ApplyTemplate method [File Server Resource Manager], ApplyTemplate method [File Server Resource Manager],IFsrmQuotaObject interface, IFsrmQuotaObject interface [File Server Resource Manager],ApplyTemplate method, IFsrmQuotaObject.ApplyTemplate, IFsrmQuotaObject::ApplyTemplate, fs.ifsrmquotaobject_applytemplate, fsrm.ifsrmquotaobject_applytemplate, fsrmquota/IFsrmQuotaObject::ApplyTemplate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmQuotaObject.ApplyTemplate
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmQuotaObject::ApplyTemplate


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Applies the property values of the specified quota template to this quota object.


## -parameters




### -param quotaTemplateName [in]

The name of the quota template.  The string is limited to 4,000 characters.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/80c01faf-717e-4375-8772-c61f04a7d7f3">IFsrmQuotaObject</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

