---
UID: NF:fsrmreports.IFsrmReport.GetFilter
title: IFsrmReport::GetFilter (fsrmreports.h)
author: windows-sdk-content
description: Retrieves the value of the specified report filter.
old-location: fsrm\ifsrmreport_getfilter.htm
tech.root: fsrm
ms.assetid: 991b0009-7ed9-4d75-af03-1b76aa8be70c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFilter, GetFilter method [File Server Resource Manager], GetFilter method [File Server Resource Manager],IFsrmReport interface, IFsrmReport interface [File Server Resource Manager],GetFilter method, IFsrmReport.GetFilter, IFsrmReport::GetFilter, fs.ifsrmreport_getfilter, fsrm.ifsrmreport_getfilter, fsrmreports/IFsrmReport::GetFilter
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
 - IFsrmReport.GetFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmReport::GetFilter


## -description


Retrieves the value of the specified report filter.


## -parameters




### -param filter [in]

The filter used to limit the files listed in a report. For possible values, see the <a href="https://msdn.microsoft.com/6f38ec9a-8876-44ce-9d44-f3982f1880ca">FsrmReportFilter</a> enumeration.


### -param filterValue [out]

The filter value for the specified report filter.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/2172a543-b3b7-453e-887b-05c8ee74f197">IFsrmReport</a>
 

 

