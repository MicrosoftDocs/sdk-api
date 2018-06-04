---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IFsrmClassificationManager interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

Manages file classification. Use this interface to define properties to use in classification, add 
    classification rules for classifying files, define classification and storage modules, and enable classification 
    reporting.

To get this interface, call the 
    <a href="_com_CoCreateInstanceEx">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmClassificationManager</b> as the class identifier and 
    <code>__uuidof(IFsrmClassificationManager)</code> as the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmClassificationManager</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFsrmClassificationManager</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ff26acfd-71ff-49f4-a7ea-60825ff42f3b">CancelClassification</a>
</td>
<td align="left" width="63%">
Cancels classification if it is running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bac42416-0757-462f-8869-339655f48587">ClearFileProperty</a>
</td>
<td align="left" width="63%">
Clears the value of the specified property in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1964f4b6-b4e0-45a2-aca1-2e3dc44745a4">CreateModuleDefinition</a>
</td>
<td align="left" width="63%">
Creates a module definition of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92c6198b-08b6-4ea6-b8de-1a21acd235d1">CreatePropertyDefinition</a>
</td>
<td align="left" width="63%">
Creates a property definition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca9a97b7-eadd-4f57-8f3a-afa439222f21">CreateRule</a>
</td>
<td align="left" width="63%">
Creates a rule of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a833e94-d26b-4c94-bf2f-76ac6db3f8e9">EnumFileProperties</a>
</td>
<td align="left" width="63%">
Enumerates the properties of the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eeda0802-e450-4a8b-a08c-135784540b17">EnumModuleDefinitions</a>
</td>
<td align="left" width="63%">
Enumerates the module definitions of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c97cb2f1-6e03-444e-a15e-faa85f7a7915">EnumPropertyDefinitions</a>
</td>
<td align="left" width="63%">
Enumerates the property definitions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f67527c-cde3-4907-9e61-4d9e18b18859">EnumRules</a>
</td>
<td align="left" width="63%">
Enumerates the rules of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8a3c4cb-4753-495b-88f4-2d6cdfef7dc7">GetFileProperty</a>
</td>
<td align="left" width="63%">
Retrieves the specified property from the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41272218-25af-4c8f-8730-37a08a7fad4f">GetModuleDefinition</a>
</td>
<td align="left" width="63%">
Retrieves the specified module definition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de89524d-70b7-4f0a-add0-d34d54bd32a7">GetPropertyDefinition</a>
</td>
<td align="left" width="63%">
Retrieves the specified property definition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c21ed09-6c69-4f03-91bb-9beeb816ed62">GetRule</a>
</td>
<td align="left" width="63%">
Retrieves the specified rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50fdc5c8-d2eb-4206-b0fa-0de2696d29c7">RunClassification</a>
</td>
<td align="left" width="63%">
Runs classification rules and generates the classification report.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f13f00e-6ca2-4436-822e-01eff638c446">SetFileProperty</a>
</td>
<td align="left" width="63%">
Sets the value of the specified property in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d288f84c-5078-40e3-ad32-6794f82157d5">WaitForClassificationCompletion</a>
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

<a href="https://msdn.microsoft.com/02c62b7d-a128-432a-a15a-51de092b5bab">ClassificationLastError</a>


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

<a href="https://msdn.microsoft.com/bdc32bbc-e8e5-48ed-97a1-0b42db3c3676">ClassificationLastReportPathWithoutExtension</a>


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

<a href="https://msdn.microsoft.com/a19a82fd-f00c-4663-b305-2cdc3bc863bd">ClassificationReportEnabled</a>


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

<a href="https://msdn.microsoft.com/a9402faa-06f9-4cfe-9a36-a2fc1a581824">ClassificationReportFormats</a>


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

<a href="https://msdn.microsoft.com/fa998edc-7ef8-43fa-a83a-7e4ba911e970">ClassificationReportMailTo</a>


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

<a href="https://msdn.microsoft.com/f0a10671-9383-4935-b773-31f047732e27">ClassificationRunningStatus</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/jj124048">Logging</a>


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
     <a href="https://msdn.microsoft.com/92c6198b-08b6-4ea6-b8de-1a21acd235d1">CreatePropertyDefinition</a>. 
     Once a property is defined it may be set using APIs such as 
     <a href="https://msdn.microsoft.com/0f13f00e-6ca2-4436-822e-01eff638c446">SetFileProperty</a>, retrieved 
     using <a href="https://msdn.microsoft.com/c8a3c4cb-4753-495b-88f4-2d6cdfef7dc7">GetFileProperty</a> or 
     <a href="https://msdn.microsoft.com/9a833e94-d26b-4c94-bf2f-76ac6db3f8e9">EnumFileProperties</a>, or 
     cleared using 
     <a href="https://msdn.microsoft.com/bac42416-0757-462f-8869-339655f48587">ClearFileProperty</a>. 
     <a href="https://msdn.microsoft.com/1dee9185-f83c-4e49-bf29-143271445046">ClassifyFiles</a> performs these 
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
     <a href="https://msdn.microsoft.com/5fb7219a-608c-43f8-a8e3-48bbf0218c6e">IFilter</a> interface to search the content of the file.

When you run classification, FSRM evaluates a files for any rule that is applicable to that file (and committed 
     to FSRM) and enabled. If reporting is enabled, FSRM also generates the classification reports.


#### Examples

For examples in C# and PowerShell see 
     <a href="https://msdn.microsoft.com/E057898F-72A0-4AB0-BE88-4C1BE6B2B5DE">Accessing Classification Properties</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

