---
UID: NN:fsrmpipeline.IFsrmClassificationManager2
title: IFsrmClassificationManager2 (fsrmpipeline.h)
author: windows-sdk-content
description: Manages file classification. Use this interface to define properties to use in classification, add classification rules for classifying files, define classification and storage modules, and enable classification reporting.
old-location: fsrm\ifsrmclassificationmanager2.htm
tech.root: fsrm
ms.assetid: 6ff821e3-f0bd-4c66-8ced-edbbfbc8503b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmClassificationManager2, IFsrmClassificationManager2 interface [File Server Resource Manager], IFsrmClassificationManager2 interface [File Server Resource Manager],described, fs.ifsrmclassificationmanager2, fsrm.ifsrmclassificationmanager2, fsrmpipeline/IFsrmClassificationManager2
ms.topic: interface
f1_keywords: 
 - "fsrmpipeline/IFsrmClassificationManager2"
dev_langs:
 - c++
req.header: fsrmpipeline.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmPipeline.idl
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
 - IFsrmClassificationManager2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmClassificationManager2 interface


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
    <code>__uuidof(IFsrmClassificationManager2)</code> as the interface 
    identifier or use the use the "Fsrm.FsrmClassificationManager" program identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmClassificationManager2</b> interface inherits from <b>IFsrmClassificationManager</b>. <b>IFsrmClassificationManager2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmClassificationManager2</b> interface has these methods.
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager2-classifyfiles">ClassifyFiles</a>
</td>
<td align="left" width="63%">
This method is used to perform bulk enumeration, setting, and clearing of file properties.

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
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmClassificationManager2</b> interface has these properties.
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


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>
 

 

