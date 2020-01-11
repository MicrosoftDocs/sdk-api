---
UID: NN:fsrmpipeline.IFsrmPipelineModuleConnector
title: IFsrmPipelineModuleConnector (fsrmpipeline.h)
description: Creates the communication channel between FSRM and your pipeline module implementation.
old-location: fsrm\ifsrmpipelinemoduleconnector.htm
tech.root: fsrm
ms.assetid: 7debbe8c-b687-42e1-b9b7-1b5f6f16a159
ms.date: 12/05/2018
ms.keywords: IFsrmPipelineModuleConnector, IFsrmPipelineModuleConnector interface [File Server Resource Manager], IFsrmPipelineModuleConnector interface [File Server Resource Manager],described, fs.ifsrmpipelinemoduleconnector, fsrm.ifsrmpipelinemoduleconnector, fsrmpipeline/IFsrmPipelineModuleConnector
f1_keywords:
- fsrmpipeline/IFsrmPipelineModuleConnector
dev_langs:
- c++
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmTlb.h
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
- IFsrmPipelineModuleConnector
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmPipelineModuleConnector interface


## -description


Creates the communication channel between FSRM and your pipeline module implementation.

Your pipeline module implementation must create this interface and To create this interface, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmFileManagementJobManager</b> as the class identifier and 
    <code>__uuidof(IFsrmFileManagementJobManager)</code> as the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmPipelineModuleConnector</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmPipelineModuleConnector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmPipelineModuleConnector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduleconnector-bind">Bind</a>
</td>
<td align="left" width="63%">
Binds the pipeline module implementation to the FSRM communication channel.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmPipelineModuleConnector</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduleconnector-get_hostingprocesspid">HostingProcessPid</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The process identifier of the module.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduleconnector-get_hostinguseraccount">HostingUserAccount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The user account under which the module runs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduleconnector-get_moduleimplementation">ModuleImplementation</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The interface that implements the pipeline module.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduleconnector-get_modulename">ModuleName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The name of the module.

</td>
</tr>
</table> 


## -remarks



Your 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduleimplementation-onload">IFsrmPipelineModuleImplementation::OnLoad</a> 
    implementation must create an instance of an object implementing this interface. To create this instance, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmPipelineModuleConnector</b> as the class identifier and 
    <code>__uuidof(IFsrmPipelineModuleConnector)</code> as the interface identifier. Use 
    the <a href="https://docs.microsoft.com/windows/desktop/api/wtypesbase/ne-wtypesbase-clsctx">CLSCTX_INPROC_SERVER</a> class context to create the instance.

After the instance has been created, 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduleconnector-bind">IFsrmPipelineModuleConnector::Bind</a> must 
    be called before you can return the instance in your 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduleimplementation-onload">OnLoad</a> implementation.

For more information on how to create and bind an instance, see 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/initializing-and-binding-a-pipeline-module">Initializing and Binding a Pipeline Module</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrmpipelinemoduleconnector">FsrmPipelineModuleConnector</a>
 

 

