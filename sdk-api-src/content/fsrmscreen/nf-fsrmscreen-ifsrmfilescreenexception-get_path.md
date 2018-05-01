---
UID: NF:fsrmscreen.IFsrmFileScreenException.get_Path
title: IFsrmFileScreenException::get_Path method
author: windows-driver-content
description: Retrieves the path that is associated with this file screen exception.
old-location: fsrm\ifsrmfilescreenexception_path.htm
old-project: Fsrm
ms.assetid: ac447042-b87b-4387-bb8f-2e69df9e7f8f
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFsrmFileScreenException, IFsrmFileScreenException interface [File Server Resource Manager], Path property, IFsrmFileScreenException.Path, IFsrmFileScreenException::get_Path, Path property [File Server Resource Manager], Path property [File Server Resource Manager], IFsrmFileScreenException interface, fs.ifsrmfilescreenexception_path, fsrm.ifsrmfilescreenexception_path, fsrmscreen/IFsrmFileScreenException::Path, fsrmscreen/IFsrmFileScreenException::get_Path, get_Path,IFsrmFileScreenException.get_Path
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmFileScreenException.Path
-	IFsrmFileScreenException.get_Path
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileScreenException::get_Path method


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1787aab2-b315-418c-81bf-1e42198c8780">MSFT_FSRMFileScreenException</a> class.]

Retrieves the path that is associated with this file screen exception.

This property is read-only.


## -parameters


## -remarks



Note that if the path is renamed, the exception becomes associated with the new path. If the path is deleted, 
    the exception is deleted.




## -see-also




<a href="https://msdn.microsoft.com/188e76dd-6df6-412f-8d51-fc727075de80">IFsrmFileScreenException</a>



<a href="https://msdn.microsoft.com/1787aab2-b315-418c-81bf-1e42198c8780">MSFT_FSRMFileScreenException</a>
 

 

