---
UID: NN:fsrmpipeline.IFsrmPipelineModuleConnector
title: IFsrmPipelineModuleConnector (fsrmpipeline.h)
author: windows-sdk-content
description: Creates the communication channel between FSRM and your pipeline module implementation.
old-location: fsrm\ifsrmpipelinemoduleconnector.htm
tech.root: fsrm
ms.assetid: 7debbe8c-b687-42e1-b9b7-1b5f6f16a159
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmPipelineModuleConnector, IFsrmPipelineModuleConnector interface [File Server Resource Manager], IFsrmPipelineModuleConnector interface [File Server Resource Manager],described, fs.ifsrmpipelinemoduleconnector, fsrm.ifsrmpipelinemoduleconnector, fsrmpipeline/IFsrmPipelineModuleConnector
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmPipelineModuleConnector interface


## -description


Creates the communication channel between FSRM and your pipeline module implementation.

Your pipeline module implementation must create this interface and To create this interface, call the 
    <a href="https://msdn.microsoft.com/en-us/library/ms680701(v=VS.85).aspx">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmFileManagementJobManager</b> as the class identifier and 
    <code>__uuidof(IFsrmFileManagementJobManager)</code> as the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmPipelineModuleConnector</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFsrmPipelineModuleConnector</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/4ac8ecc7-a02e-46ce-ac95-35a7dd38e631">Bind</a>
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

<a href="https://msdn.microsoft.com/bd9259de-35e4-46e9-9994-388c3ac77172">HostingProcessPid</a>


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

<a href="https://msdn.microsoft.com/c5935160-81e9-4e2a-88ac-a37d2a78fcff">HostingUserAccount</a>


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

<a href="https://msdn.microsoft.com/0399ffd6-39c1-40fe-8cfa-c627bbd59680">ModuleImplementation</a>


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

<a href="https://msdn.microsoft.com/ef64a255-94da-4d42-af90-1ac9b2c0fbbc">ModuleName</a>


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
    <a href="https://msdn.microsoft.com/69d848b9-4143-4b6c-9a45-66ff44c54b66">IFsrmPipelineModuleImplementation::OnLoad</a> 
    implementation must create an instance of an object implementing this interface. To create this instance, call the 
    <a href="https://msdn.microsoft.com/en-us/library/ms680701(v=VS.85).aspx">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmPipelineModuleConnector</b> as the class identifier and 
    <code>__uuidof(IFsrmPipelineModuleConnector)</code> as the interface identifier. Use 
    the <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX_INPROC_SERVER</a> class context to create the instance.

After the instance has been created, 
    <a href="https://msdn.microsoft.com/4ac8ecc7-a02e-46ce-ac95-35a7dd38e631">IFsrmPipelineModuleConnector::Bind</a> must 
    be called before you can return the instance in your 
    <a href="https://msdn.microsoft.com/69d848b9-4143-4b6c-9a45-66ff44c54b66">OnLoad</a> implementation.

For more information on how to create and bind an instance, see 
    <a href="https://msdn.microsoft.com/92568969-7ee6-4584-a400-ee2aa79961e8">Initializing and Binding a Pipeline Module</a>.




## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/b00f4d1f-2920-4ec4-ae90-756b2600198b">FsrmPipelineModuleConnector</a>
 

 

