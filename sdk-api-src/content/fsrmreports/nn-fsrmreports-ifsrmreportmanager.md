---
UID: NN:fsrmreports.IFsrmReportManager
title: IFsrmReportManager (fsrmreports.h)
description: Used to manage report jobs.
helpviewer_keywords: ["IFsrmReportManager","IFsrmReportManager interface [File Server Resource Manager]","IFsrmReportManager interface [File Server Resource Manager]","described","fs.ifsrmreportmanager","fsrm.ifsrmreportmanager","fsrmreports/IFsrmReportManager"]
old-location: fsrm\ifsrmreportmanager.htm
tech.root: fsrm
ms.assetid: 112ed457-1083-4550-abd6-933f4b128e9a
ms.date: 12/05/2018
ms.keywords: IFsrmReportManager, IFsrmReportManager interface [File Server Resource Manager], IFsrmReportManager interface [File Server Resource Manager],described, fs.ifsrmreportmanager, fsrm.ifsrmreportmanager, fsrmreports/IFsrmReportManager
req.header: fsrmreports.h
req.include-header: FsrmReports.h, FsrmTlb.h
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
 - IFsrmReportManager
 - fsrmreports/IFsrmReportManager
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
 - IFsrmReportManager
---

# IFsrmReportManager interface


## -description

Used to manage report jobs.

To get this interface, call the 
    <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmReportManager</b> as the class identifier and 
    <code>__uuidof(IFsrmReportManager)</code> as the interface identifier. For 
    an example, see <a href="/previous-versions/windows/desktop/fsrm/defining-a-report-job">Defining a Report Job</a>.

## -inheritance

The <b>IFsrmReportManager</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmReportManager</b> also has these types of members:

## -remarks

A storage report job specifies a set of directories that will be analyzed to generate one or more different 
    report types that help administrators to better understand how storage is utilized in the specified directories. 
    You can configure report jobs to execute according to a schedule or on demand.

To create this object from a script, use the "Fsrm.FsrmReportManager" program 
    identifier.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/fsrm/fsrmreportmanager">FsrmReportManager</a>
