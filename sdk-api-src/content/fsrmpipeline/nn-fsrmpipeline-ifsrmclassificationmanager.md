---
UID: NN:fsrmpipeline.IFsrmClassificationManager
title: IFsrmClassificationManager (fsrmpipeline.h)
author: windows-sdk-content
description: Manages file classification. Use this interface to define properties to use in classification, add classification rules for classifying files, define classification and storage modules, and enable classification reporting.
old-location: fsrm\ifsrmclassificationmanager.htm
tech.root: fsrm
ms.assetid: cc504f6c-00d7-4f9d-9688-1c29b5066ce6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmClassificationManager, IFsrmClassificationManager interface [File Server Resource Manager], IFsrmClassificationManager interface [File Server Resource Manager],described, fs.ifsrmclassificationmanager, fsrm.ifsrmclassificationmanager, fsrmpipeline/IFsrmClassificationManager
ms.topic: interface
f1_keywords: 
 - "fsrmpipeline/IFsrmClassificationManager"
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
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
 - IFsrmClassificationManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmClassificationManager interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

Manages file classification. Use this interface to define properties to use in classification, add 
    classification rules for classifying files, define classification and storage modules, and enable classification 
    reporting.

To get this interface, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmClassificationManager</b> as the class identifier and 
    <code>__uuidof(IFsrmClassificationManager)</code> as the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmClassificationManager</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmClassificationManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmClassificationManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-cancelclassification">CancelClassification</a>
</td>
<td align="left" width="63%">
Cancels classification if it is running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-clearfileproperty">ClearFileProperty</a>
</td>
<td align="left" width="63%">
Clears the value of the specified property in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createmoduledefinition">CreateModuleDefinition</a>
</td>
<td align="left" width="63%">
Creates a module definition of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createpropertydefinition">CreatePropertyDefinition</a>
</td>
<td align="left" width="63%">
Creates a property definition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createrule">CreateRule</a>
</td>
<td align="left" width="63%">
Creates a rule of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumfileproperties">EnumFileProperties</a>
</td>
<td align="left" width="63%">
Enumerates the properties of the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enummoduledefinitions">EnumModuleDefinitions</a>
</td>
<td align="left" width="63%">
Enumerates the module definitions of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumpropertydefinitions">EnumPropertyDefinitions</a>
</td>
<td align="left" width="63%">
Enumerates the property definitions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumrules">EnumRules</a>
</td>
<td align="left" width="63%">
Enumerates the rules of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getfileproperty">GetFileProperty</a>
</td>
<td align="left" width="63%">
Retrieves the specified property from the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getmoduledefinition">GetModuleDefinition</a>
</td>
<td align="left" width="63%">
Retrieves the specified module definition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getpropertydefinition">GetPropertyDefinition</a>
</td>
<td align="left" width="63%">
Retrieves the specified property definition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getrule">GetRule</a>
</td>
<td align="left" width="63%">
Retrieves the specified rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-runclassification">RunClassification</a>
</td>
<td align="left" width="63%">
Runs classification rules and generates the classification report.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-setfileproperty">SetFileProperty</a>
</td>
<td align="left" width="63%">
Sets the value of the specified property in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-waitforclassificationcompletion">WaitForClassificationCompletion</a>
</td>
<td align="left" width="63%">
Waits for the specified period of time or until classification has finished running.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmClassificationManager</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_classificationlasterror">ClassificationLastError</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The error message from the last time classification was run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_classificationlastreportpathwithoutextension">ClassificationLastReportPathWithoutExtension</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The local directory path where the reports were stored the last time classification ran.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_classificationreportenabled">ClassificationReportEnabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Determines whether classification reporting is enabled or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_classificationreportformats">ClassificationReportFormats</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The list of formats in which to generate the classification reports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_classificationreportmailto">ClassificationReportMailTo</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The email address to which to send the classification reports, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_classificationrunningstatus">ClassificationRunningStatus</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The running status of classification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-get_logging">Logging</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The types of logging to perform when running the classification rules.

</td>
</tr>
</table> 


## -remarks



To create this object from a script, use the "Fsrm.FsrmClassificationManager" program 
    identifier.

The classification feature lets you classify (tag) files. To do this the properties that can be associated with 
     a file must first be defined using 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createpropertydefinition">CreatePropertyDefinition</a>. 
     Once a property is defined it may be set using APIs such as 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-setfileproperty">SetFileProperty</a>, retrieved 
     using <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getfileproperty">GetFileProperty</a> or 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumfileproperties">EnumFileProperties</a>, or 
     cleared using 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-clearfileproperty">ClearFileProperty</a>. 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager2-classifyfiles">ClassifyFiles</a> performs these 
     actions on multiple files. Alternatively a series of rules to automatically classify files can be created. If a 
     rule applies to the file, the rule associates a property and property value with the file. The property can be 
     stored separately from the file or stored in the file depending on the storage module available on the 
     machine.

The built-in System Cache Storage Module stores the properties outside of the file using alternate data stream 
     storage and the security descriptor (Windows Server 2012 and Windows 8 only). Storing the 
     properties separately may result in them not moving when the file is moved.

The Office Storage Modules store the classification properties in the Office files themselves. One parser is 
     for Office 97-2003 files, and the other is for Office 2007-2010 files. Office files that contain the 
     classification properties in the file can have the properties displayed in SharePoint if the property names match 
     the SharePoint column names. Updating the column values in SharePoint updates the properties in the file. Note 
     that SharePoint treats these names as case-sensitive, therefore the property definition's name defined in FSRM 
     must have the same case when uploading to SharePoint.

You can use the classification and storage plugins or you can implement your own classification and storage 
     plugins. Note that the built-in Content Classifier plugin uses the 
     <a href="https://docs.microsoft.com/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> interface to search the content of the file.

When you run classification, FSRM evaluates a files for any rule that is applicable to that file (and committed 
     to FSRM) and enabled. If reporting is enabled, FSRM also generates the classification reports.


#### Examples

For examples in C# and PowerShell see 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/accessing-classification-properties">Accessing Classification Properties</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>
 

 

