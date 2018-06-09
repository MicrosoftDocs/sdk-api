---
UID: NF:fsrmscreen.IFsrmFileScreen.get_Path
title: IFsrmFileScreen::get_Path
author: windows-sdk-content
description: Retrieves the directory path associated with the file screen object.
old-location: fsrm\ifsrmfilescreen_path.htm
old-project: Fsrm
ms.assetid: 383e829c-5089-4404-a6bd-429812069e85
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IFsrmFileScreen interface [File Server Resource Manager],Path property, IFsrmFileScreen.Path, IFsrmFileScreen.get_Path, IFsrmFileScreen::Path, IFsrmFileScreen::get_Path, Path property [File Server Resource Manager], Path property [File Server Resource Manager],IFsrmFileScreen interface, fs.ifsrmfilescreen_path, fsrm.ifsrmfilescreen_path, fsrmscreen/IFsrmFileScreen::Path, fsrmscreen/IFsrmFileScreen::get_Path, get_Path
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
 - IFsrmFileScreen.Path
 - IFsrmFileScreen.get_Path
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileScreen::get_Path


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/86ee74e0-64d5-478a-8150-0f4b37e56694">MSFT_FSRMFileScreen</a> class.]

Retrieves the directory path associated with the file screen object.

This property is read-only.


## -parameters


## -remarks



Note that the file screen remains associated with the directory if the directory is renamed. If the directory 
    is deleted, so is the file screen.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/298e7e37-709a-4b13-87d3-605d540d8f85">Updating a File Screen</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/69b831a1-c935-4de0-b222-009bafc45ec5">IFsrmFileScreen</a>



<a href="https://msdn.microsoft.com/86ee74e0-64d5-478a-8150-0f4b37e56694">MSFT_FSRMFileScreen</a>
 

 

