---
UID: NF:fsrmscreen.IFsrmFileScreen.ApplyTemplate
title: IFsrmFileScreen::ApplyTemplate
author: windows-sdk-content
description: Applies the property values of the specified file screen template to this file screen object.
old-location: fsrm\ifsrmfilescreen_applytemplate.htm
old-project: fsrm
ms.assetid: d495cb92-09c4-4fa5-873c-5f07475eb7bf
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: ApplyTemplate, ApplyTemplate method [File Server Resource Manager], ApplyTemplate method [File Server Resource Manager],IFsrmFileScreen interface, IFsrmFileScreen interface [File Server Resource Manager],ApplyTemplate method, IFsrmFileScreen.ApplyTemplate, IFsrmFileScreen::ApplyTemplate, fs.ifsrmfilescreen_applytemplate, fsrm.ifsrmfilescreen_applytemplate, fsrmscreen/IFsrmFileScreen::ApplyTemplate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmscreen.h
req.include-header: 
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
 - IFsrmFileScreen.ApplyTemplate
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileScreen::ApplyTemplate


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/86ee74e0-64d5-478a-8150-0f4b37e56694">MSFT_FSRMFileScreen</a> class.]

Applies the property values of the specified file screen template to this file screen 
    object.


## -parameters




### -param fileScreenTemplateName [in]

The name of the file screen template. The string is limited to 4,000 characters.


## -returns



The method returns the following return values.




## -remarks



To save the changes, call the 
    <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmFileScreen::Commit</a> method.

The specified template must be a committed template; you cannot apply a newly created template that has not 
    been committed.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/1b5227e7-4272-4e23-ba55-d6161e2987bc">Defining a File Screen</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/69b831a1-c935-4de0-b222-009bafc45ec5">IFsrmFileScreen</a>



<a href="https://msdn.microsoft.com/86ee74e0-64d5-478a-8150-0f4b37e56694">MSFT_FSRMFileScreen</a>
 

 

