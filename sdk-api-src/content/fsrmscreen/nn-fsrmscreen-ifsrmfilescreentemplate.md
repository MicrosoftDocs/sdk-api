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
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreentemplate">MSFT_FSRMFileScreenTemplate</a> class.]

Used to configure templates from which new file screens can be derived. Templates are 
    identified by a name and are used to simplify configuration of file screens.

To create this interface, call the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplatemanager-createtemplate">IFsrmFileScreenTemplate::CreateTemplate</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplatemanager-enumtemplates">IFsrmFileScreenTemplate::EnumTemplates</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplatemanager-gettemplate">IFsrmFileScreenTemplate::GetTemplate</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplatemanager-importtemplates">IFsrmFileScreenTemplate::ImportTemplates</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileScreenTemplate</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenbase">IFsrmFileScreenBase</a>. <b>IFsrmFileScreenTemplate</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplate-commitandupdatederived">CommitAndUpdateDerived</a>
</td>
<td align="left" width="63%">
Saves the file screen template and then applies any changes to the derived file screen objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplate-copytemplate">CopyTemplate</a>
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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplate-get_name">Name</a>


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenbase">IFsrmFileScreenBase</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreentemplate">MSFT_FSRMFileScreenTemplate</a>
 

 

