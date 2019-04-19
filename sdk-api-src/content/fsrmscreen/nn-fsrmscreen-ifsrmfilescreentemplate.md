---
UID: NN:fsrmscreen.IFsrmFileScreenTemplate
title: IFsrmFileScreenTemplate (fsrmscreen.h)
author: windows-sdk-content
description: Used to configure templates from which new file screens can be derived.
old-location: fsrm\ifsrmfilescreentemplate.htm
tech.root: fsrm
ms.assetid: c8e612f5-e7cd-45ff-9eaf-9d1674231161
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmFileScreenTemplate, IFsrmFileScreenTemplate interface [File Server Resource Manager], IFsrmFileScreenTemplate interface [File Server Resource Manager],described, fs.ifsrmfilescreentemplate, fsrm.ifsrmfilescreentemplate, fsrmscreen/IFsrmFileScreenTemplate
ms.topic: interface
req.header: fsrmscreen.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmScreen.idl
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
 - IFsrmFileScreenTemplate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmFileScreenTemplate interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/be4f3a6a-280f-4b0f-afdf-ce1ee7933018">MSFT_FSRMFileScreenTemplate</a> class.]

Used to configure templates from which new file screens can be derived. Templates are 
    identified by a name and are used to simplify configuration of file screens.

To create this interface, call the 
    <a href="https://msdn.microsoft.com/3d654dee-2a27-4dc0-8e2b-fba546abe17e">IFsrmFileScreenTemplate::CreateTemplate</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/5bfb82f9-50a5-4266-956d-f99e2982a6a5">IFsrmFileScreenTemplate::EnumTemplates</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e97149f6-8cf5-433c-a487-799322253e44">IFsrmFileScreenTemplate::GetTemplate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0660a1cb-904e-4ed0-bbc8-9903e8848f4e">IFsrmFileScreenTemplate::ImportTemplates</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileScreenTemplate</b> interface inherits from <a href="https://msdn.microsoft.com/9e52af8c-e03b-4b44-83bd-541fe1419d6c">IFsrmFileScreenBase</a>. <b>IFsrmFileScreenTemplate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmFileScreenTemplate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b50a93f-f6f0-4ab4-a4a3-3995b721c5d7">CommitAndUpdateDerived</a>
</td>
<td align="left" width="63%">
Saves the file screen template and then applies any changes to the derived file screen objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6c69f15-9a7c-43f4-9d68-a54c333453f5">CopyTemplate</a>
</td>
<td align="left" width="63%">
Copies the property values of the specified template to this template.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileScreenTemplate</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b72309d1-8b8e-46bc-bca4-e6e47dae88e8">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves and sets the name of the file screen template.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/9e52af8c-e03b-4b44-83bd-541fe1419d6c">IFsrmFileScreenBase</a>



<a href="https://msdn.microsoft.com/be4f3a6a-280f-4b0f-afdf-ce1ee7933018">MSFT_FSRMFileScreenTemplate</a>
 

 

