---
UID: NN:fhcfg.IFhConfigMgr
title: IFhConfigMgr (fhcfg.h)
author: windows-sdk-content
description: The IFhConfigMgr interface allows client applications to read and modify the File History configuration for the user account under which the methods of this interface are called.
old-location: winprog\ifhconfigmgr.htm
tech.root: DevNotes
ms.assetid: CDE8A011-6E78-49DF-A5E1-8E968355BA11
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFhConfigMgr, IFhConfigMgr interface [Windows API], IFhConfigMgr interface [Windows API],described, fhcfg/IFhConfigMgr, winprog.ifhconfigmgr
ms.topic: interface
f1_keywords: ["fhcfg/IFhConfigMgr"]
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
ms.custom: 19H1
---

# IFhConfigMgr interface


## -description


The <b>IFhConfigMgr</b> interface allows client applications to read and modify the File History configuration for the user account under which the methods of this interface are called.

> [!NOTE] 
> **IFhConfigMgr** is deprecated and may be altered or unavailable in future releases.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFhConfigMgr</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFhConfigMgr</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-addremoveexcluderule">AddRemoveExcludeRule</a>
</td>
<td align="left" width="63%">
Adds an exclusion rule to the exclusion list or removes a  rule from the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-changedefaulttargetrecommendation">ChangeDefaultTargetRecommendation</a>
</td>
<td align="left" width="63%">
Causes the currently assigned backup target to be recommended or not recommended to other members of the home group that the computer belongs to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-createdefaultconfiguration">CreateDefaultConfiguration</a>
</td>
<td align="left" width="63%">
Creates File History configuration files with default settings for the current user and loads them into an <a href="https://docs.microsoft.com/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getbackupstatus">GetBackupStatus</a>
</td>
<td align="left" width="63%">
Retrieves the backup status value for an <a href="https://docs.microsoft.com/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getdefaulttarget">GetDefaultTarget</a>
</td>
<td align="left" width="63%">
Returns a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nn-fhcfg-ifhtarget">IFhTarget</a> interface that can be used to query information about the currently assigned backup target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getincludeexcluderules">GetIncludeExcludeRules</a>
</td>
<td align="left" width="63%">
Retrieves the inclusion and exclusion rules that are currently stored in an <a href="https://docs.microsoft.com/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getlocalpolicy">GetLocalPolicy</a>
</td>
<td align="left" width="63%">
Retrieves the numeric parameter for a local policy for the File History feature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-loadconfiguration">LoadConfiguration</a>
</td>
<td align="left" width="63%">
Loads the File History configuration information for the current user into an <a href="https://docs.microsoft.com/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-provisionandsetnewtarget">ProvisionAndSetNewTarget</a>
</td>
<td align="left" width="63%">
Provisions a certain storage device or network share as a File History backup target and assigns it as the default backup target for the current user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-queryprotectionstatus">QueryProtectionStatus</a>
</td>
<td align="left" width="63%">
Retrieves the current File History protection state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-saveconfiguration">SaveConfiguration</a>
</td>
<td align="left" width="63%">
Saves to disk all the changes that were made in an <a href="https://docs.microsoft.com/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a> object since the last time that the <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-loadconfiguration">LoadConfiguration</a>, <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-createdefaultconfiguration">CreateDefaultConfiguration</a> or <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-saveconfiguration">SaveConfiguration</a> method was called  for the File History configuration files of the current user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-setbackupstatus">SetBackupStatus</a>
</td>
<td align="left" width="63%">
Changes the backup status value for an <a href="https://docs.microsoft.com/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-setlocalpolicy">SetLocalPolicy</a>
</td>
<td align="left" width="63%">
Changes the numeric parameter value of a local policy in an <a href="https://docs.microsoft.com/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-validatetarget">ValidateTarget</a>
</td>
<td align="left" width="63%">
 Checks whether a certain storage device or network share can be used as a File History backup target.

</td>
</tr>
</table> 

