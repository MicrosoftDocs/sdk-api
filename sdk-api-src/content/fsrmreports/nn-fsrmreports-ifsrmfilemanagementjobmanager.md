---
UID: NN:fsrmreports.IFsrmFileManagementJobManager
title: IFsrmFileManagementJobManager (fsrmreports.h)
author: windows-sdk-content
description: Used to manage file management jobs.
old-location: fsrm\ifsrmfilemanagementjobmanager.htm
tech.root: fsrm
ms.assetid: 2df0e8d0-1da7-422e-8d02-ad5d030fdd8d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmFileManagementJobManager, IFsrmFileManagementJobManager interface [File Server Resource Manager], IFsrmFileManagementJobManager interface [File Server Resource Manager],described, fs.ifsrmfilemanagementjobmanager, fsrm.ifsrmfilemanagementjobmanager, fsrm/IFsrmFileManagementJobManager
ms.topic: interface
f1_keywords: ["fsrmreports/IFsrmFileManagementJobManager"]
req.header: fsrmreports.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
 - IFsrmFileManagementJobManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmFileManagementJobManager interface


## -description


Used to manage file management jobs.

To get this interface, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmFileManagementJobManager</b> as the class identifier and 
    <code>__uuidof(IFsrmFileManagementJobManager)</code> as the interface 
    identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileManagementJobManager</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmFileManagementJobManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmFileManagementJobManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-createfilemanagementjob">CreateFileManagementJob</a>
</td>
<td align="left" width="63%">
Creates a file management job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-enumfilemanagementjobs">EnumFileManagementJobs</a>
</td>
<td align="left" width="63%">
Enumerates the list of existing file management jobs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-getfilemanagementjob">GetFileManagementJob</a>
</td>
<td align="left" width="63%">
Gets the specified file management job.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileManagementJobManager</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-get_actionvariabledescriptions">ActionVariableDescriptions</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the descriptions for the macros contained in the 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-get_actionvariables">ActionVariables</a> 
     property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-get_actionvariables">ActionVariables</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a  list of macros that you can specify in action property values.

</td>
</tr>
</table> 


## -remarks



To create this object from a script, use the "Fsrm.FsrmFileManagementJobManager" program identifier.

A file management job consumes the classification properties associated with a file. The job performs actions 
    based whether the property values set by classification meet the specified file management property conditions. 
    The primary action is to expire the file (move the file to an expired files folder) and send notification that the 
    file was expired; however, you can also perform custom actions.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrmfilemanagementjobmanager">FsrmFileManagementJobManager</a>
 

 

