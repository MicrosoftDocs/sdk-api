---
UID: NF:fsrmreports.IFsrmReport.Delete
title: IFsrmReport::Delete
author: windows-sdk-content
description: Removes this report object from the report job object.
old-location: fsrm\ifsrmreport_delete.htm
tech.root: Fsrm
ms.assetid: b50139bc-c584-4bed-bf2e-34f1fef16e6d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Delete, Delete method [File Server Resource Manager], Delete method [File Server Resource Manager],IFsrmReport interface, IFsrmReport interface [File Server Resource Manager],Delete method, IFsrmReport.Delete, IFsrmReport::Delete, fs.ifsrmreport_delete, fsrm.ifsrmreport_delete, fsrmreports/IFsrmReport::Delete
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFsrmReport.Delete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- fsrmreports.h
: 
- IFsrmReport.Delete
: 
---

# IFsrmReport::Delete


## -description


Removes this report object from the report job object.


## -parameters






## -returns



The method returns the following return values.




## -remarks



Note that the reports are not deleted until you call the <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmReportJob::Commit</a> method.




## -see-also




<a href="https://msdn.microsoft.com/2172a543-b3b7-453e-887b-05c8ee74f197">IFsrmReport</a>



<a href="https://msdn.microsoft.com/ea8a3f6b-326b-4c8f-a6fc-7b7525c5543f">IFsrmReportJob</a>
 

 

