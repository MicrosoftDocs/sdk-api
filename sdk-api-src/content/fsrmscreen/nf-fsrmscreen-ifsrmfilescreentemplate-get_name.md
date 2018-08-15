---
UID: NF:fsrmscreen.IFsrmFileScreenTemplate.get_Name
title: IFsrmFileScreenTemplate::get_Name
author: windows-sdk-content
description: Retrieves and sets the name of the file screen template.
old-location: fsrm\ifsrmfilescreentemplate_name.htm
old-project: fsrm
ms.assetid: b72309d1-8b8e-46bc-bca4-e6e47dae88e8
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: IFsrmFileScreenTemplate interface [File Server Resource Manager],Name property, IFsrmFileScreenTemplate.Name, IFsrmFileScreenTemplate.get_Name, IFsrmFileScreenTemplate::Name, IFsrmFileScreenTemplate::get_Name, IFsrmFileScreenTemplate::put_Name, Name property [File Server Resource Manager], Name property [File Server Resource Manager],IFsrmFileScreenTemplate interface, fs.ifsrmfilescreentemplate_name, fsrm.ifsrmfilescreentemplate_name, fsrmscreen/IFsrmFileScreenTemplate::Name, fsrmscreen/IFsrmFileScreenTemplate::get_Name, fsrmscreen/IFsrmFileScreenTemplate::put_Name, get_Name
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmscreen.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmScreen.idl
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
 - IFsrmFileScreenTemplate.Name
 - IFsrmFileScreenTemplate.get_Name
 - IFsrmFileScreenTemplate.put_Name
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileScreenTemplate::get_Name


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/be4f3a6a-280f-4b0f-afdf-ce1ee7933018">MSFT_FSRMFileScreenTemplate</a> class.]

Retrieves and sets the name of the file screen template.

This property is read/write.


## -parameters


## -remarks



If a template with the specified name exists, the template fails with 
    <b>FSRM_E_ALREADY_EXISTS</b> when you call the 
    <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmFileScreen::Commit</a> method.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/c76c0cc5-1109-46ec-be4d-c6c5f14a6df7">Using Templates to Define File Screens</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/c8e612f5-e7cd-45ff-9eaf-9d1674231161">IFsrmFileScreenTemplate</a>



<a href="https://msdn.microsoft.com/be4f3a6a-280f-4b0f-afdf-ce1ee7933018">MSFT_FSRMFileScreenTemplate</a>
 

 

