---
UID: NF:fsrmreports.IFsrmReportJob.EnumReports
title: IFsrmReportJob::EnumReports
author: windows-sdk-content
description: Enumerates all the reports configured for this report job.
old-location: fsrm\ifsrmreportjob_enumreports.htm
tech.root: Fsrm
ms.assetid: a1292084-f1b5-43eb-9b59-fa2f3f99557d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EnumReports, EnumReports method [File Server Resource Manager], EnumReports method [File Server Resource Manager],IFsrmReportJob interface, IFsrmReportJob interface [File Server Resource Manager],EnumReports method, IFsrmReportJob.EnumReports, IFsrmReportJob::EnumReports, fs.ifsrmreportjob_enumreports, fsrm.ifsrmreportjob_enumreports, fsrmreports/IFsrmReportJob::EnumReports
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
 - IFsrmReportJob.EnumReports
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
- IFsrmReportJob.EnumReports
: 
---

# IFsrmReportJob::EnumReports


## -description


Enumerates all the reports configured for this report job.


## -parameters




### -param reports [out]

An <a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a> interface that contains a collection of reports. The collection is empty if no reports are defined for the job.

Each item of the collection is a <b>VARIANT</b> of type <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member to get the <a href="https://msdn.microsoft.com/2172a543-b3b7-453e-887b-05c8ee74f197">IFsrmReport</a> interface.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/ea8a3f6b-326b-4c8f-a6fc-7b7525c5543f">IFsrmReportJob</a>
 

 

