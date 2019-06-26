---
UID: NN:fhcfg.IFhReassociation
title: IFhReassociation (fhcfg.h)
author: windows-sdk-content
description: This interface allows client applications to reassociate a File History configuration from a File History target with the current user.
old-location: winprog\ifhreassociation.htm
tech.root: DevNotes
ms.assetid: B1CBD7DD-5B4D-4B3E-BE7D-B6497ABFB588
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFhReassociation, IFhReassociation interface [Windows API], IFhReassociation interface [Windows API],described, fhcfg/IFhReassociation, winprog.ifhreassociation
ms.topic: interface
f1_keywords: 
 - "fhcfg/IFhReassociation"
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
 - IFhReassociation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFhReassociation interface


## -description


This interface allows client applications to reassociate a File History configuration from a File History target with the current user. Reassociation serves two purposes:<ul>
<li>It allows the user to access the data that was backed up to the target in the past, possibly from a different computer or under a different account.</li>
<li>It allows the user to continue to back up data to the target, possibly on a new computer or under a new account name.</li>
</ul>

> [!NOTE] 
> **IFhReassociation** is deprecated and may be altered or unavailable in future releases.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFhReassociation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFhReassociation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFhReassociation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-getconfigurationdetails">GetConfigurationDetails</a>
</td>
<td align="left" width="63%">
This method enumerates File History configurations that were discovered on a storage device or network share by the <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-scantargetforconfigurations">IFhReassociation::ScanTargetForConfigurations</a> method and returns additional information about each of the discovered configurations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-performreassociation">PerformReassociation</a>
</td>
<td align="left" width="63%">
This method re-establishes relationship between the current user and the configuration selected previously via the <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-selectconfiguration">IFhReassociation::SelectConfiguration</a> method and prepares the target device for accepting backup data from the current computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-scantargetforconfigurations">ScanTargetForConfigurations</a>
</td>
<td align="left" width="63%">
Scans the namespace on a specified storage device or network share for File History configurations that can be reassociated with and continued to be used on the current computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-selectconfiguration">SelectConfiguration</a>
</td>
<td align="left" width="63%">
Selects one of the File History configurations discovered on a storage device or network share by the <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-scantargetforconfigurations">IFhReassociation::ScanTargetForConfigurations</a> method for subsequent reassociation. Actual reassociation is performed by the <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-performreassociation">IFhReassociation::PerformReassociation</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-validatetarget">ValidateTarget</a>
</td>
<td align="left" width="63%">
 This method checks whether a certain storage device or network share can be used as a File History default target and, thus, whether reassociation is possible at all or not.

</td>
</tr>
</table> 

