---
UID: NN:fhcfg.IFhReassociation
title: IFhReassociation
author: windows-sdk-content
description: This interface allows client applications to reassociate a File History configuration from a File History target with the current user.
old-location: winprog\ifhreassociation.htm
tech.root: devnotes
ms.assetid: B1CBD7DD-5B4D-4B3E-BE7D-B6497ABFB588
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IFhReassociation, IFhReassociation interface [Windows API], IFhReassociation interface [Windows API],described, fhcfg/IFhReassociation, winprog.ifhreassociation
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
 - IFhReassociation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFhReassociation interface


## -description


This interface allows client applications to reassociate a File History configuration from a File History target with the current user. Reassociation serves two purposes:<ul>
<li>It allows the user to access the data that was backed up to the target in the past, possibly from a different computer or under a different account.</li>
<li>It allows the user to continue to back up data to the target, possibly on a new computer or under a new account name.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFhReassociation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFhReassociation</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/4B5259B7-D845-4CF1-AC33-56DF9D00F2E2">GetConfigurationDetails</a>
</td>
<td align="left" width="63%">
This method enumerates File History configurations that were discovered on a storage device or network share by the <a href="https://msdn.microsoft.com/E26F5C41-50E7-4D4F-A6FF-D1B21AF28A9D">IFhReassociation::ScanTargetForConfigurations</a> method and returns additional information about each of the discovered configurations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2E80F25E-2DB6-4522-8F3C-7E6359104CCA">PerformReassociation</a>
</td>
<td align="left" width="63%">
This method re-establishes relationship between the current user and the configuration selected previously via the <a href="https://msdn.microsoft.com/5501F87D-2998-4CB7-B9C8-9EC04F42B22D">IFhReassociation::SelectConfiguration</a> method and prepares the target device for accepting backup data from the current computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E26F5C41-50E7-4D4F-A6FF-D1B21AF28A9D">ScanTargetForConfigurations</a>
</td>
<td align="left" width="63%">
Scans the namespace on a specified storage device or network share for File History configurations that can be reassociated with and continued to be used on the current computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5501F87D-2998-4CB7-B9C8-9EC04F42B22D">SelectConfiguration</a>
</td>
<td align="left" width="63%">
Selects one of the File History configurations discovered on a storage device or network share by the <a href="https://msdn.microsoft.com/E26F5C41-50E7-4D4F-A6FF-D1B21AF28A9D">IFhReassociation::ScanTargetForConfigurations</a> method for subsequent reassociation. Actual reassociation is performed by the <a href="https://msdn.microsoft.com/2E80F25E-2DB6-4522-8F3C-7E6359104CCA">IFhReassociation::PerformReassociation</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/307F2C8F-B847-437C-BDD7-BE09FD407C79">ValidateTarget</a>
</td>
<td align="left" width="63%">
 This method checks whether a certain storage device or network share can be used as a File History default target and, thus, whether reassociation is possible at all or not.

</td>
</tr>
</table> 

