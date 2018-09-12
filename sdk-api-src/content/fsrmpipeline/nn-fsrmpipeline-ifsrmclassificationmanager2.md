---
UID: NN:fsrmpipeline.IFsrmClassificationManager2
title: IFsrmClassificationManager2
author: windows-sdk-content
description: Manages file classification. Use this interface to define properties to use in classification, add classification rules for classifying files, define classification and storage modules, and enable classification reporting.
old-location: fsrm\ifsrmclassificationmanager2.htm
tech.root: fsrm
ms.assetid: 6ff821e3-f0bd-4c66-8ced-edbbfbc8503b
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: IFsrmClassificationManager2, IFsrmClassificationManager2 interface [File Server Resource Manager], IFsrmClassificationManager2 interface [File Server Resource Manager],described, fs.ifsrmclassificationmanager2, fsrm.ifsrmclassificationmanager2, fsrmpipeline/IFsrmClassificationManager2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmClassificationManager2 interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

Manages file classification. Use this interface to define properties to use in classification, add 
    classification rules for classifying files, define classification and storage modules, and enable classification 
    reporting.

To get this interface, call the 
    <a href="https://msdn.microsoft.com/en-us/library/ms680701(v=VS.85).aspx">CoCreateInstanceEx</a> function. Use 
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
<a href="https://msdn.microsoft.com/ff26acfd-71ff-49f4-a7ea-60825ff42f3b">CancelClassification</a>
</td>
<td align="left" width="63%">
Cancels classification if it is running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1dee9185-f83c-4e49-bf29-143271445046">ClassifyFiles</a>
</td>
<td align="left" width="63%">
This method is used to perform bulk enumeration, setting, and clearing of file properties.

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
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmClassificationManager2</b> interface has these properties.
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

<a href="https://msdn.microsoft.com/c22f646b-36dc-45b8-a9ad-81ce6adab5bf">Logging</a>


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




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

