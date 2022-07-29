---
UID: NF:fsrmreports.IFsrmReport.get_Name
title: IFsrmReport::get_Name (fsrmreports.h)
description: Retrieves or sets the name of the report. (Get)
helpviewer_keywords: ["IFsrmReport interface [File Server Resource Manager]","Name property","IFsrmReport.Name","IFsrmReport.get_Name","IFsrmReport::Name","IFsrmReport::get_Name","IFsrmReport::put_Name","Name property [File Server Resource Manager]","Name property [File Server Resource Manager]","IFsrmReport interface","fs.ifsrmreport_name","fsrm.ifsrmreport_name","fsrmreports/IFsrmReport::Name","fsrmreports/IFsrmReport::get_Name","fsrmreports/IFsrmReport::put_Name","get_Name"]
old-location: fsrm\ifsrmreport_name.htm
tech.root: fsrm
ms.assetid: 4fde46af-1d13-4ca8-b627-0285c694fb6e
ms.date: 12/05/2018
ms.keywords: IFsrmReport interface [File Server Resource Manager],Name property, IFsrmReport.Name, IFsrmReport.get_Name, IFsrmReport::Name, IFsrmReport::get_Name, IFsrmReport::put_Name, Name property [File Server Resource Manager], Name property [File Server Resource Manager],IFsrmReport interface, fs.ifsrmreport_name, fsrm.ifsrmreport_name, fsrmreports/IFsrmReport::Name, fsrmreports/IFsrmReport::get_Name, fsrmreports/IFsrmReport::put_Name, get_Name
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmReport::get_Name
 - fsrmreports/IFsrmReport::get_Name
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmReport.Name
 - IFsrmReport.get_Name
 - IFsrmReport.put_Name
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
     <a href="/previous-versions/windows/desktop/fsrm/adding-a-report-to-a-job">Adding a Report to a Job</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreport">IFsrmReport</a>
