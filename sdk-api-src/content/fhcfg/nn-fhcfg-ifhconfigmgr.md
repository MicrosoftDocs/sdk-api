---
UID: NN:fhcfg.IFhConfigMgr
title: IFhConfigMgr
author: windows-sdk-content
description: The IFhConfigMgr interface allows client applications to read and modify the File History configuration for the user account under which the methods of this interface are called.
old-location: winprog\ifhconfigmgr.htm
tech.root: devnotes
ms.assetid: CDE8A011-6E78-49DF-A5E1-8E968355BA11
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IFhConfigMgr, IFhConfigMgr interface [Windows API], IFhConfigMgr interface [Windows API],described, fhcfg/IFhConfigMgr, winprog.ifhconfigmgr
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fhcfg.h
api_name:
 - IFhConfigMgr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFhConfigMgr interface


## -description


The <b>IFhConfigMgr</b> interface allows client applications to read and modify the File History configuration for the user account under which the methods of this interface are called.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFhConfigMgr</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFhConfigMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFhConfigMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8900944D-3B73-49AB-AE26-F0B2D5842B02">AddRemoveExcludeRule</a>
</td>
<td align="left" width="63%">
Adds an exclusion rule to the exclusion list or removes a  rule from the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40F22464-FE28-40A0-85C6-74C5BD819E83">ChangeDefaultTargetRecommendation</a>
</td>
<td align="left" width="63%">
Causes the currently assigned backup target to be recommended or not recommended to other members of the home group that the computer belongs to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70F67D8D-E449-4006-BB14-0E5E9B91D517">CreateDefaultConfiguration</a>
</td>
<td align="left" width="63%">
Creates File History configuration files with default settings for the current user and loads them into an <a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0AC8F205-B593-4117-9059-0DDA5BBE3124">GetBackupStatus</a>
</td>
<td align="left" width="63%">
Retrieves the backup status value for an <a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/570CB5FD-7586-41AD-84A6-DA6966B18E91">GetDefaultTarget</a>
</td>
<td align="left" width="63%">
Returns a pointer to an <a href="https://msdn.microsoft.com/5A73A81A-72A3-4794-86E5-9CA8FCA200C0">IFhTarget</a> interface that can be used to query information about the currently assigned backup target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DE137C08-923D-4ADC-8EBC-2F277F72CAE4">GetIncludeExcludeRules</a>
</td>
<td align="left" width="63%">
Retrieves the inclusion and exclusion rules that are currently stored in an <a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/380B77C3-CA93-48D6-9915-FB788CF24C99">GetLocalPolicy</a>
</td>
<td align="left" width="63%">
Retrieves the numeric parameter for a local policy for the File History feature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9959AF70-87C2-45E0-A409-959494AF393B">LoadConfiguration</a>
</td>
<td align="left" width="63%">
Loads the File History configuration information for the current user into an <a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9C9FA696-CFB2-4814-96D5-2B9B6A2AB426">ProvisionAndSetNewTarget</a>
</td>
<td align="left" width="63%">
Provisions a certain storage device or network share as a File History backup target and assigns it as the default backup target for the current user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/662B1F54-D50D-4434-BD81-DF600D28B573">QueryProtectionStatus</a>
</td>
<td align="left" width="63%">
Retrieves the current File History protection state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71D6E732-927B-4AA4-9947-6E52B09FF5B8">SaveConfiguration</a>
</td>
<td align="left" width="63%">
Saves to disk all the changes that were made in an <a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a> object since the last time that the <a href="https://msdn.microsoft.com/9959AF70-87C2-45E0-A409-959494AF393B">LoadConfiguration</a>, <a href="https://msdn.microsoft.com/70F67D8D-E449-4006-BB14-0E5E9B91D517">CreateDefaultConfiguration</a> or <a href="https://msdn.microsoft.com/71D6E732-927B-4AA4-9947-6E52B09FF5B8">SaveConfiguration</a> method was called  for the File History configuration files of the current user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17FF01A1-028D-4A22-A64C-F24C98F86663">SetBackupStatus</a>
</td>
<td align="left" width="63%">
Changes the backup status value for an <a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A1106349-6B14-4A44-B845-7853FA1919D6">SetLocalPolicy</a>
</td>
<td align="left" width="63%">
Changes the numeric parameter value of a local policy in an <a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EC41C4EE-A909-4DD4-AA32-5054BBEAF421">ValidateTarget</a>
</td>
<td align="left" width="63%">
 Checks whether a certain storage device or network share can be used as a File History backup target.

</td>
</tr>
</table> 

