---
UID: NF:fsrmreports.IFsrmReport.get_Name
title: IFsrmReport::get_Name
author: windows-sdk-content
description: Retrieves or sets the name of the report.
old-location: fsrm\ifsrmreport_name.htm
old-project: Fsrm
ms.assetid: 4fde46af-1d13-4ca8-b627-0285c694fb6e
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: IFsrmReport interface [File Server Resource Manager],Name property, IFsrmReport.Name, IFsrmReport.get_Name, IFsrmReport::Name, IFsrmReport::get_Name, IFsrmReport::put_Name, Name property [File Server Resource Manager], Name property [File Server Resource Manager],IFsrmReport interface, fs.ifsrmreport_name, fsrm.ifsrmreport_name, fsrmreports/IFsrmReport::Name, fsrmreports/IFsrmReport::get_Name, fsrmreports/IFsrmReport::put_Name, get_Name
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmreports.h
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
-	IFsrmReport.Name
-	IFsrmReport.get_Name
-	IFsrmReport.put_Name
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmReport::get_Name


## -description


Retrieves or sets the name of the report.

This property is read/write.


## -parameters


## -remarks



If not set, FSRM generates a unique name for you.

The name is used in the report.  If email notification is sent, the subject contains the report name.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/2dd5420b-33ab-4831-83b8-a9a4b2201a60">Adding a Report to a Job</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2172a543-b3b7-453e-887b-05c8ee74f197">IFsrmReport</a>
 

 

